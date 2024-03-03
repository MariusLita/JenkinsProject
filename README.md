This project is an simple app which opens a html page ( template was download from tooplate.com ) on the localhost of the device.

For this project i have been used Spring Boot and use mvn to run it.

After you clone the repo you will have to follow the next steps to run the application:

	mvn clean instal
	mvn spring-boot:run

This two commands will install the dependecies based on the pom.xml file and run the SpringBoot app.
To test it just access localhost:8080 on an browser and you should be able to see the html template.


The project also contains the Jenkinsfile if you want to run the project in Jenkins.

