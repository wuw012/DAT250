# DAT250 - Expass 6

## Experiment 1: Model-View-Controller Web Applications
I had some issues creating a runnable JAR, seems like a lot others also had this issue and that the command to create a JAR file should be:

 `mvn clean install && java -jar target/serving-web-content-initial-0.0.1-SNAPSHOT.jar`

Also had some issues again pushing a previously cloned git module to git :) Resolved by `git rm --cached . -rf` and `rm -rf .git`

## Experiment 2: Single-page applications
I faced some CORS errors and had to get help from Thomas to resolve them with providing http headers.
Other than that I though Angular had a steep learning curve even though I am pretty comfortable working in frontend.

Repo: https://github.com/wuw012/dat250-expass6
