# REST web service using Dropwizard along with UI interface in React
![image](https://user-images.githubusercontent.com/62707309/143731209-32ffcbce-e848-400c-87c9-85a4bf736bb6.png)


### Functionality
The web service takes in a numerical value between 1 to 100, and returns the Fibonacci sequence, as well as a sequence that is sorted using the following conditions:
* Even numbers first, in descending order
* Odd numbers, in descending order


### Example: 
If user does a http get to http://myserver:8000/fibonacci with the following json payload:
```json

{
 "elements": 10
} 
```

it will return me the following JSON:
```json
{
 "fibonacci": [0,1,1,2,3,5,8,13,21,34],
 "sorted": [34,8,2,0,21,13,5,3,1,1]
}
```



# Dependencies

* Maven dropwizard-core
* Maven Jersey-moxy

```
    <dependencies>
        <!-- https://mvnrepository.com/artifact/io.dropwizard/dropwizard-core -->
        <dependency>
            <groupId>io.dropwizard</groupId>
            <artifactId>dropwizard-core</artifactId>
            <version>2.0.25</version>
        </dependency>
        
        <!-- https://mvnrepository.com/artifact/org.glassfish.jersey.media/jersey-media-moxy -->
        <dependency>
            <groupId>org.glassfish.jersey.media</groupId>
            <artifactId>jersey-media-moxy</artifactId>
            <version>2.34</version>
        </dependency>
    </dependencies>
</
```


# Port confifuration

The application port is set at 9090 and admin port is at 9091

```
String applicationPort = "9090";
String adminPort = "9091";
```

Please change the port numbers in ~/Program file if needed


# CORS headers has been handled

Configuration
```
cors.setInitParameter("allowedOrigins", "*");
cors.setInitParameter("allowedHeaders", "X-Requested-With,Content-Type,Accept,Origin");
cors.setInitParameter("allowedMethods", "OPTIONS,GET,PUT,POST,DELETE,HEAD");

```


# Testing

## Using Postman 
![image](https://user-images.githubusercontent.com/62707309/143731067-efed4905-de65-421f-9073-3a44ff7b041b.png)
API side message:
![image](https://user-images.githubusercontent.com/62707309/143731165-a0c76b41-932a-4676-aa19-d5e407ae484d.png)



## Using React Web app
![image](https://user-images.githubusercontent.com/62707309/143731126-3f0219e8-5ce7-4522-9043-96c7c222dd5b.png)
API side message:
![image](https://user-images.githubusercontent.com/62707309/143731153-c703752f-9587-4024-a360-bac1403308b9.png)

