# DAT250 - Expass 3

## Installation
- The correct validation of the installation package 
<img width="573" alt="Screen Shot 2022-11-21 at 22 10 56" src="https://user-images.githubusercontent.com/56112778/203158930-3abda3d0-c582-4dfb-8257-dbf2b1a5a1f6.png">


## Experiment 1: MongoDB CRUD operations
- insertmany()
<img width="641" alt="Screen Shot 2022-11-21 at 22 16 59" src="https://user-images.githubusercontent.com/56112778/203159842-a99917fc-c1e1-4e8e-a11c-dddf01112c88.png">

- find() with query
<img width="626" alt="Screen Shot 2022-11-21 at 22 17 44" src="https://user-images.githubusercontent.com/56112778/203159952-950db6df-a2f8-4442-b020-ae84855eedbf.png">

- updateMany()
<img width="455" alt="Screen Shot 2022-11-21 at 22 19 28" src="https://user-images.githubusercontent.com/56112778/203160209-64548b39-ad92-470b-b026-3c5540a9805d.png">

- deleteOne()
<img width="488" alt="Screen Shot 2022-11-21 at 22 21 20" src="https://user-images.githubusercontent.com/56112778/203160523-9d85ce94-a9f5-4366-90a7-2d816de65646.png">

- bulkWrite()
<img width="644" alt="Screen Shot 2022-11-21 at 22 22 27" src="https://user-images.githubusercontent.com/56112778/203160658-47c70dc2-622e-469c-be84-7de68e71945f.png">

## Experiment 2: Aggregation

- map reduce working
<img width="656" alt="Screen Shot 2022-11-21 at 22 26 55" src="https://user-images.githubusercontent.com/56112778/203161372-4b58bd3e-d3fc-4d56-a12d-02ac1dd39fcb.png">

- my own example
```
db.students.insertMany([
{ "name" : "Ingvild", "subject" : "science", "marks" : 68 }, 
{ "name" : "Ingvild", "subject" : "maths", "marks" : 98 },
{ "name" : "Jonas", "subject" : "sports", "marks" : 77 },
{ "name" : "Thomas", "subject" : "science", "marks" : 67 },
{ "name" : "Jonas", "subject" : "maths", "marks" : 87 },
])
var map = function() {emit(this.name,this.marks);};
var reduce = function(name,marks) {return Array.sum(marks);};

db.students.mapReduce(
   map,
   reduce,
   { out: "totals" }
);
```
<img width="699" alt="Screen Shot 2022-11-21 at 22 37 50" src="https://user-images.githubusercontent.com/56112778/203163160-fc30c557-2763-429f-ae18-eda02615f988.png">
