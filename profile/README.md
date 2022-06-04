## Useful commands:

### Jira with Github
- add the Jira issue key when commiting e.g. `git commit -m "PROJ-123 add a README file to the project."`
- checkout a new branch with an issue key e.g. `git checkout -b JRA-123-<branch-name>`
      
### Docker 

#### Docker Compose
run docker-compose.yml (docker-compose file has to be in pwd)
      
      docker-compose up
      
(Container are automatically build)
      
#### CLI:
 Build Docker Spring Image
      
      docker build -t springio/[NAME] .
      
 Run Spring Image in Container
      
      docker run -p [DOCKER PORT]:[LOCAL PORT] springio/[NAME]
      
 Run and install lightweight postgres image locally (password and username here as in warehouse app-prod.properties):
      
      docker run --name postgres_test_db -e POSTGRES_PASSWORD=test_password -e POSTGRES_USER=test_user -p 5432:5432 -d postgres:13.1-alpine

 


---

## Quick Guides:

### Postman
Quick Definition: Tool for working with/testing API.

#### Testing API
1. Run your API in IntelliJ
2. Open Postman App 
3. Go to your collection or create one
4. Add a request and name it "<<Collection_Name>> API Test" 
5. Choose the GET-Method and enter your API e.g. "http://localhost:8080/YOUR_PATH"
6. Click "SEND"
7. Status 200 OK: Means successful
8. View the output below in "Pretty" or "Raw"

Useful Links: https://www.youtube.com/watch?v=E0f9DUEN_jI&t=3s

#### Testing possible incorrect requests
- Use snippets on the right of Postman App
- Test different values

##

### Swagger
#### Quick Info
Quick Definition: Useful for documenting APIs, also allows to make requests via documentation

**Dependency for Swagger:** 

io.springfox -> springfox-swagger2, version: 3.0.0

**Enabeling Swagger**

Add tag "@EnableSwagger2" below tag "@SpringBootApplication" in Main Class to enable Swagger

**Annotations Swagger will recognize**

@GetMapping for GET endpoints, @PostMapping for POST endpoints, @PutMapping, @DeleteMapping, @PatchMapping ...

Hide endpoints by prefacing with tag "@Hidden"

**Using Swagger with Postman**

To see Swagger documentation in Postman, use {port}/v2/api-docs after starting application

#### SwaggerUI
Quick Definition: HTML Swagger documentation

**Dependency for Swagger:** 

io.springfox -> springfox-boot-starter, version: 3.0.0

**Using Swagger UI**

For Swagger UI documentation, go to {port}/swagger-ui/ in your browser (the "/" being vital). You can also start HTTP requests from the interface without the need of Postman.

##
      
### H2
      
**How to use**
      
There are two options to test the local DB with H2-
      
Option 1: Using the H2 Client
      
Option 2: Using the web console 
      
These options don't differ much. Just make sure you're on the right URL and port, and using the proper credentials, and you'll be fine. You can check them in Warehouse -> application.properties. 
      
**H2 Client**
      
1. Download client here: https://www.h2database.com/html/download.html
When using OS other than Windows, see https://o7planning.org/11895/install-h2-database-and-use-h2-console for help running the client.
2. After starting the Spring App, run the H2 client and log in.
      
**Browser client**
      
The Spring App is configured to enable using a browser client. 
1. After starting the Spring App, go to {port}/console and log in. 
      
**Interacting with the database**
      
After connecting to the H2DB, you should see three tables: component, product, and products_components. Currently, they should be empty after starting the app. You can run regular SQL commands to interact with the database, for example "SELECT * FROM component;" to see all components in the DB and their attributes. 

You can add data to the DB using SQL statements, it is recommended though that you use HTTP requests. For this, you can use _Swagger UI_ or _Postman_. There are some predesigned  HTTP requests available to workspace members in Postman ready to use in the collection "Hibernate API test".

### REACT Bootstrap
1. npx create-react-app << project name >>
2. npm install react-bootstrap bootstrap
3. add bootstrap styles: go to project and open public/index.html and insert the following in the head section below the last link section
      <link
      rel="stylesheet"
      href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css"
      integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3"
      crossorigin="anonymous"
    />
  
### REACT Router
1. npm instsall react-router-dom
  
Note: If you are using a npm version lower than 5.0.0 then add the "--save" flag to add the dependency to your package.json
Note 2: Depending on version above or below 5, <Switch> and <Routes> sections changes: 
        https://exerror.com/attempted-import-error-switch-is-not-exported-from-react-router-dom/
      
