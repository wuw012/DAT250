# DAT250: FIRST LAB REPORT

## Technical problems with installation

Struggled with installation of Maven. Solved it by adding it to path and editing the 
JAVA_HOME variable since it was referencing the wrong/old jdk.
Also struggeled with psql command for PostgreSQL where it told 
me I entered the wrong password. Pretty sure I was typing in the right password. Tried ident/admin and other default passwords. Also tried to 


## Validating software

+ mvn: by mvn clean install and seeing "BUILD FAILURE"
+ java: java --version in cmd
+ intellij: opened it
+ git: already installed (git status for validating)
+ postgresql: 

## Heroku setup

+ Followed guide, all fine until setting up local PostgreSQL database 
+ Added the `/bin` folder to my PATH. 
+ Set up a Heroku account
+ Installed Heroku with a Windows installer
+ Cloned a Git repository with a web app 
+ Deployed my first Heroku web app: validated with `heroku open`, read the logs with `heroku logs --tail`
+ Tried to setup a local database with `psql` instead of `heroku psql`. 
  + Asked for a password, put in what I believed to be right. 
  + Access denied.
  + 102384 tries later I concluded that something was wrong and the password I entered had to be right. 
  + Tried to change the .conf file in PostgreSQL. Didnt work 
  + Reinstalling postgres had no effect. 
  + Decided to skip this local setup part for now.


[Link to the web app.](https://boiling-taiga-46526.herokuapp.com/)
