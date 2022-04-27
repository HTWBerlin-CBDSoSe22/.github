## Useful commands:

### Jira with Github
- add the Jira issue key when commiting e.g. `git commit -m "PROJ-123 add a README file to the project."`
- checkout a new branch with an issue key e.g. `git checkout -b JRA-123-<branch-name>`

### IntelliJ
- find and replace:
- > command + R



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


