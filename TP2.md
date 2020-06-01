# TP 2

## Build and test your application

### Ok, what is it supposed to do ?

```bash
mvn clean verirfy
```

This command will actually clear your previous builds inside your cache (otherwise your can have unexpected behavior because maven did not build again each part of your application), then it will freshly build each module inside your application and finally it will run both Unit Tests and Integration Tests (sometime called Component Tests as well) defined in the application and return whether it was successful or not..

### What are Unit tests ? Integration test ?

Unit tests are supposed to check if one functionality of an application work as expected sometimes Unit tests check the correct expectations of a simple function.

Integration test checks if functionalities work between each other.
Integration tests require a database to verify you correctly inserted or retrieved data from inside

### What is a db changelog job ?

A db changelog job is meant to maintain database versioning

### What are testcontainers?

Simply are java libraries that allow you to run a bunch of docker containers while testing. A java library that run docker "lightweight, throwaway instances" to test common databases.


### Why do we need this branch ?

This branch is needed because we don't want to commit changes on the main branch which would be actually running our application. In which case, build might pass, but screw up our application.

### Secured variables, why ?

We use Secured variables so they dont show up in our source code to protect our repositories. 

### Why do we need this ?

We need these Dockerfiles so the pipeline will be able to build our images, this way, it will also test our build.

### For what purpose ?

This way, we'll be able not only to versionize our code, but also our builds. This way, we'll be able to back in time.
