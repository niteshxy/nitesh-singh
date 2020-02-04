Rest API test automation with [Tavern](https://tavern.readthedocs.io/en/latest/)

This solution provides a way to automate API tests.
[Swagger petstore](https://github.com/swagger-api/swagger-petstore) sample app is used for sample api server.

#### Prerequisites
##### 1. Docker and docker compose should be installed
#
#
#### Steps to run
1. Clone the [Swagger petstore](https://github.com/swagger-api/swagger-petstore) repository.
2. Run the server with Maven , using this command -
```
mvn package jetty:run
```
3. Clone this [repository](https://github.com/niteshxy/nitesh-singh) of this task.
4. Navigate to the "APITests" directory
5. Open the common.yaml file and replace the ip of the "base_url" to the ip of the machine where swagger-petstore server is running.
6. Navigate to the "APITests" directory in the terminal and run
```
docker-compose up
```

#### Test cases which are automated

##### Pets
1. /findByStatus GET request.
2. /pet POST request
3. /pet GET request to find pet by ID
4. /pet DELETE request to delete pet by ID
5. Check the /pet GET request with deleted pet id
6. /pet GET request with invalid pet id


#### Store
1. /inventory GET request
2. /order POST request
3. /order DELETE request to delete order by id
4. /order GET request for deleted oder

#### User
1. /user POST request to create a user
2. /login GET request
3. /logout GET request
4. /user GET request to get user by username
5. /user DELETE request to delete user by username
6. /user GET request for deleted user


#### Framework details

##### Why Tavern
This framework is built in [tavern](https://tavern.readthedocs.io/en/latest/)
Tavern is very lightweight and easy to use tool for Rest Api test automation, it uses pytest under the hood and all the capabilities of pytest can be extended by tavern.
It can be used to write simple as well as complex test scenarios. Seperate functions can be written in python and used by tavern yaml files if needed in complex cases.

#### Explanation of this framework
The tests in tavern are written in YAML files. In APItests directory there are 3 yaml files for testing pet, user and store endpoints.
In tavern, the tests follow simple yaml syntax where request is sent and response is validated. The command to run the tests in given in docker-compose.yaml file in "api-tests" service. By default all the files which are named in the format "test_*.tavern.yaml" will be run by tavern.
At the end of the test execution the result (number of passed and failed tests) is shown in the console.


