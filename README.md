# Restful Web Service built with Spring

This repository is for a Web Service built with Java and Spring Boot, this particular service, will accept a http get request and will respond with a Json.

# Running application

Building an executable jar makes it easy to ship, version, and deploy the service as an application throughout the development lifecycle, across different environments, and so forth.

You can build the JAR file with ./mvnw clean package (MacOS)/mvnw clean package (Windows) and then run the JAR file, as follows:

java -jar target/rest-service-0.1.0.jar

Now, you should be able to visit http://localhost:8080/greeting and see an output:

{"id":1,"content":"Hello, World!"}

Provide a name query string parameter by visiting http://localhost:8080/greeting?name=User. Notice how the value of the content attribute changes from Hello, World! to Hello, User!, as the following listing shows:

{"id":2,"content":"Hello, User!"}

This change demonstrates that the @RequestParam arrangement in GreetingController is working as expected. The name parameter has been given a default value of World but can be explicitly overridden through the query string.

Notice also how the id attribute has changed from 1 to 2. This proves that you are working against the same GreetingController instance across multiple requests and that its counter field is being incremented on each call as expected.