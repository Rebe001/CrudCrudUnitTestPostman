# CrudCrud REST api test

## Table of contents
* [Introduction](#introduction)
* [Test Scenario Category](#test-scenario-category)
* [Test Action](#test-action)
* [How to run test case](#how-to-run-test-case)
* [Built with](#built-with)
* [Author](#author)

## Introduction
This project is a part of CRUD API REST demo. Please visit test plan and integration testing for more details.

This postman project is to automate unit tests for the API Rest. API creation is supported by Crud Crud http://crudcrud.com, and resources `chargers` has been created.
Here are the list of APIs that will be tested in this project:

![image](https://user-images.githubusercontent.com/23367428/142723521-8b5e9b51-5c65-4fa8-9b28-cf0ea31d86e6.png)


## Test Scenario Category

* Unit testing: Test all individual software modules (API calls) separated
* Positive testing: Create an entity, Read all entities, Read an entity, Update an entity, Delete an entity
- Negative testing: non Json schema, invalid id (absent id, non guid format id, non existing id, special character id)

## Test Action

* Test cases may use one/more test actions: 
- Verify http header content type
- Verify http status code
- Verify response payload is not null
- Verify response body is (not) array
- Verify field type and field value
- Verify id set automatically

## How to run test case
* download collection `Chargers.postman_collection.json` and enviroment variable `CrudCrud.postman_environment.json` from repository
* import and upload collection and enviroment variable
* select `CrudCrud` as enviroment variable
* select `Chargers`as collection and run collection
* test result displays:
![image](https://user-images.githubusercontent.com/23367428/142723804-a5a1afa7-5b74-42a7-8f50-c36bc008c663.png)


 Get and set `endpoint identifier` during run collection:
* run request `Get endpoint identifier from crud crud`
* get html response from crudcrud.com
* get endpoint identifies from html classname and attributes
* set it as postman environment variable `endpoint identifier`
* so this enviroment variable can be reused in other testcases 

 Get and set `id` during run collection:
* run request `Create a charger entity`
* convert response body to json schema and set `_id` as postman environment variable `id`
* so this enviroment variable can be reused in other testcases 

Or you can run each testcases:
* go to each request and click the send test button
* go to Tests tab and test result will be display in Test Results section
   
## Built with
* Postman
* Javascript

## Author
* Contributor: Rebecca
* Date: 19/11/2021
