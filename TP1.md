# Backend simple app

### Are you able to contact your SpringBook application through a web browser?

- We are not because no port has been defined

# Explore your API other endpoints, have a look at the controllers in the source code, explain each endpoint found in each controller

## GreetingController.java

### GET

endpoint : "/"

Display the number of times this endpoint has been called.

This endpoint can receive one argument : name 

If no argument is given default value is "World" otherwise the content value is "hello name!"

## DepartmentController.java

### GET

Endpoint : "/departments"

Display departments from database.

Endpoint : "/departments/{departmentName}/students"

Display Students by {departmentName}

Endpoint : "/departments/{departmentName}"

Display {departmentName} id and name 

Endpoint : "/departments/{departmentName}/count"

Display the number of Stundents in {departmentName}


## StudentsController.java

### GET

Endpoint : "/students"

Display students and their department (instead of just the id) from database.

Endpoint : "/students/{id}"

Display student with id {id}

### POST

Endpoint : "/students"

create and display a Student

### PUT

Endpoint : "/students/{id}"

Update and display the Student with {id} ( the entire Student is updated )


### DELETE

Endpoint : "/students/{id}"

Delete the student with id {id}

Controllers use departmentService et StudentService to call the DB.

### What are the useful docker-compose sub-commands?

docker-compose offers interesting commands such as 'down' wich stop and remove all containers, networks, images, and volumes ran by that docker-compose file.
