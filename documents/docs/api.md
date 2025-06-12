# api route

## Auth

 | Method | Route          | Purpose                              |
 |:------ |:--------------:|:------------------------------------:|
 |POST    | /auth/register | Register a new user                  |
 |POST    | /auth/login    | Login user and return token/settion  |
 |PUT    | /auth/edit     | Change the password of existing user |


 ## Credentials


 | Method | Route                    | Purpose                              |
 |:-------|:------------------------:|:------------------------------------:|
 | GET    | /credentials             | Get the list of a user's credentials |
 | POST   | /credential              | register a new credential            |
 | POST    | /credentials/:id/reveal | Get revealed password                |
 | PUT    | /credentials/:id         | update credential                    |
 | DELETE | /credentials/:id         | Delete the credential                |
