#Motivation
This little application is for showing the possibility to deploy "old school" applications inside container native environments.

It shows how to transform old school fashioned applications in a fast and efficient manner to fulfill cloud native paradigms.

##Modules
This project contains several mandatory files:

* pom.xml : Containing all dependencies for the Java logic
* Dockerfile : Containing all information for the container image
* src/main/java/HybridIT/DemoUI.java : All logic to create a running UI
* src/main/java/HybridIT/com/fourspaces/[util]/*.java : Logic to communicate with the couchDB

##How to run this application
The user has to create the image itself (I included the --no-cache flag since I had several problems with my internet connectivity- the download stopped and the Docker engine used the broken packages from the cache... Annoying ;) ):

_ sudo docker build --no-cache �t java:ui . _

After the build process finished, the user can run the couchDB and the UI automatically by running the shell script.
Please have in mind that the container environment does not support stateful applications. If you want to save the entries of the DB, please checkout the couchDB & Docker container manuals (or write me a message, I'll give you some hints :) ).

##Functionality

The application runs an UI in which user can create entries and submit them to the couchDB.

The user can retrieve the information of the DB- but cannot delete the entries of the DB again. I will extend the application by this feature in the next weeks.

##Closing words
If you find a bug, or something else, please contact me. If you want to get some background information, feel free to contact me. If you have some feedback, contact me... If you have something else, contact me (which surprise).