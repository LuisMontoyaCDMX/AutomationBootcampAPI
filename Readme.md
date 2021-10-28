READ ME
--------
Last update: Oct 28, 2021


1. PROJECT NAME
------------

Automation Bootcamp API Testing

2. GENERAL INFO
------------

This is a collection of tests using postman.  These are aimed to test the API of the 'todoist' site.

3. STRUCTURE
------------
There are 3 files in the repository:

-Readme.md :  this document
-Todoist.postman_collection.json : the collection of tests (explained below)
-Todoist.postman_environment.json :  the environment variables

The contents of the collection is distribuited as follows:

Todoist
 |
 ├ Projects(folder)-┬-Get all projects
 |                  ├ Create a new project
 |                  ├ Get a project
 |                  ├ Update a project
 |                  ├ Deleta a project
 |                  └ Negatives(folder) ┬ Cannot get all projects
 |                                      ├ Cannot create a new project
 |                                      ├ Cannot get a project
 |                                      ├ Cannot update a project
 |                                      └ Cannot delete a project
 └ Tasks  (folder) -┬-Get active tasks
                    ├ Create a new task
                    ├ Get an active task
                    ├ Update a task
                    ├ Close a task
                    ├ Reopen a task
                    ├ Deleta a task
                    └ Negatives(folder) ┬ Cannot get active tasks
                                        ├ Cannot create a new task
                                        ├ Cannot get an active task
                                        ├ Cannot update a task
                                        ├ Cannot close a task
                                        ├ Cannot reopen a task         
                                        └ Cannot delete a project
                                        
4. USAGE
---------

The purpose of each test is described as follows:

Get all projects: returns all of the projects in Todoist contains the following tests:
    1. Verifies that the Status code is 200
    
Create a new project: creates a new project in Todoist, contains the following tests:
    1. Pre-request script that sets the projectName environment var
    2. Sets the projectID env var with the response from the API
    3. Verifies that the status code is 200
    4. Cleans up the projectName env var
    
Get a project: returns a specific project by projectId, contains the following tests:
    1. Verifies that the status code is 200
    2. Validates the SCHEMA of the response

Update a project: updates some values of the project, contains the following tests:
    1. Verifies that the status code is 204
    2. Validate that the CONTENT-TYPE header is present
    3. Validate the value of the CONTENT-TYPE header
    
Deleta a project: deletes a project, , contaits the following tests:
    1. Verifies that the status code is 204
    
Cannot get all projects: Negative test to verify that we cannot retrieve all projects with a request with invalid data, it contains the following tests:
        1. Verifies that the status code is 404
        
Cannot create a new project: Negative test to verify that we cannot create a new project with a request with invalid data, it contains the following tests:
        1. Verifies that the status code is 500

Cannot get a project: Negative test to verify that we cannot retrieve a project with a request with invalid data, it contains the following tests:
        1. Verifies that the status code is 404
        
Cannot update a project: Negative test to verify that we cannot update a project with a request with invalid data, it contains the following tests:
        1. Verifies that the status code is 500
        
Cannot delete a project: Negative test to verify that we cannot delete a project with a request with invalid data, it contains the following tests:
        1. Verifies that the status code is 500
        
Get active tasks: returns all of the tasks in Todoist, contains the following tests:
    1. Verifies that the Status code is 200
    
Create a new task: creates a new task in Todoist, contains the following tests:
    1. Pre-request script that sets the taskName environment var
    2. Sets the taskId env var with the response from the API
    3. Verifies that the status code is 200
    4. Cleans up the taskName env var
    
Get an active task: returns a specific task by taskId, contains the following tests:
    1. Verifies that the status code is 200
    2. Validates a property of the json file of the response against an env variable with a value extracted from the previous test
    
Update a task: updates some values of the task, contains the following tests:
    1. Verifies that the status code is 204
    
Close a task: closes a specifc task, contains the following tests:
        1. Verifies that the status code is 204
        
Reopen a task: reopens a specifc task, contains the following tests:
        1. Verifies that the status code is 204
        
Deleta a task: deletes a specifc task, contains the following tests:
        1. Verifies that the status code is 204
        
Cannot get active tasks: Negative test to verify that we cannot retrieve all tasks with a request with invalid data, it contains the following tests:
        1. Verifies that the status code is 404
        
Cannot create a new task: Negative test to verify that we cannot create a new task with a request with invalid data, it contains the following tests:
        1. Verifies that the status code is 404
        
Cannot get an active task: Negative test to verify that we cannot retrieve a specific task with a request with invalid data, it contains the following tests:
        1. Verifies that the status code is 404
        
Cannot update a task: Negative test to verify that we cannot update a task with a request with invalid data, it contains the following tests:
        1. Verifies that the status code is 404
        
Cannot close a task: Negative test to verify that we cannot close a task with a request with invalid data, it contains the following tests:
        1. Verifies that the status code is 404
        
Cannot reopen a task: Negative test to verify that we cannot reopen a task with a request with invalid data, it contains the following tests:
        1. Verifies that the status code is 404    
             
Cannot delete a project: Negative test to verify that we cannot delete a task with a request with invalid data, it contains the following tests:
        1. Verifies that the status code is 404

 
 5. CREDITS
 ----------
 
 Developed and maintained by:
 Luis Cuauhtemoc Montoya (Wizeline) luis.cuauhtemoc@wizeline.com

