## Useful commands:

### Jira with Github
- add the Jira issue key when commiting e.g. `git commit -m "PROJ-123 add a README file to the project."`
- checkout a new branch with an issue key e.g. `git checkout -b JRA-123-<branch-name>`

### IntelliJ
- replace all ";" to "," for example
- > command + R



---

## Quick Guides:

### Postman

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
