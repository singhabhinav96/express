Create a user login and registration system using email, password combination.

  - Use express-generator to create a new application in root directory(basic_auth)

  - a user should be able to register with name, email, password
  - should be able to hash password before saving it to database(use bcrypt).
  - use pre('save') hooks and schema methods to hash and validate password respectively
  - a user should be able to login using email/password 
  - use express-session to create a session for each logged user
  - implement logout 
  - add basic authorization
    - only a logged user should be able to navigate to index('/') route.