# DAT250 - Expass 4

### Experiment 1: Spark/Java Framework project and Postman
Everything went fine! Forgot to include the body for the PUT request at first but quickly realized

### Experiment 2: REST API for TODO-items
Passing 3/7 tests. However, when trying them out for myself in Postman i see that they all actually work. Have been stuck on this issue for some time now
and have tried different approaches, but none have proven successful. 

Not passing, but works in postman: 
- testReadOne
- testUpdate
- testIdNotANumber 
- testNonExistingTodo

Here is a link to my github: https://github.com/wuw012/dat250-sparkjava-counter.git
Below Ive written a little about the pending issues and what I have tried together with some pictures. 


#### JsonSyntaxException
With the first two (testReadOne, testUpdate) I get this error.
```
[qtp1838403937-23] INFO spark.http.matching.MatcherFilter - The requested route [/todos/6] has not been mapped in Spark for Accept: [null]
com.google.gson.JsonSyntaxException: java.lang.IllegalStateException: Expected BEGIN_OBJECT but was STRING at line 1 column 1 path $
```
After some googling it seems like my JSON starts with " instead of {. I've tried converting it with GSON using toJson method a few different ways but havent
managed to figure it out




#### 404 Not Found instead of error message
For the last two I recieve a 404 Not found error message, but in Postman the correct error message is shown. Below you will find some pictures of Postman.


##### PUT : Not a number error
<img width="899" alt="Screen Shot 2022-11-21 at 17 41 12" src="https://user-images.githubusercontent.com/56112778/203111024-b912a72f-a62b-4e53-8c12-130ef870109c.png">

##### DELETE : Not a number error
<img width="893" alt="Screen Shot 2022-11-21 at 17 41 54" src="https://user-images.githubusercontent.com/56112778/203111211-e2411392-8883-40d8-9991-4408a340d917.png">

##### PUT : ID not found
<img width="860" alt="Screen Shot 2022-11-21 at 17 40 13" src="https://user-images.githubusercontent.com/56112778/203110863-f252036a-612a-4cf3-85ee-38ec748681e6.png">

##### DELETE : ID not found
<img width="900" alt="Screen Shot 2022-11-21 at 17 44 44" src="https://user-images.githubusercontent.com/56112778/203111826-f11362d7-3873-4421-9091-6677c6fb090a.png">
