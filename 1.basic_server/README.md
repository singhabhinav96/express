1. Convert your portfolio into an express application
  folder structure
  app.js // express server
  public
    - images // for all images
    - stylesheets // for css
    - js // for static js
  package.json
  templates
    - all html files


  - create single route for single page portfolio.
  - for multiple html pages, display them by creating multiple routes

Example: 
  for 3 routes ie. '/', '/about', '/projects' create different routes in app.js
  ```js
  app.get('/', (req, res) => {
    res.sendFile(__dirname + '/templates/index.html')
  })
  ```

  - use sendFile method to read HTMl files and send them in response.

2. create a basic server in express with following(don't use generators)
  - add listener on port 3000.
  - create a middleware that console logs current date on each request.
  - create a middleware that console logs url of each request.
  - create a middleware that logs 'welcome user' when request is made on /users.
  - create a middleware that logs 'page not found' when request is made on '/404'
  - create a error handler middleware with 4 arguments that sends 'server error' in response when error is passed as argument to next function.
  - create a middleware which works as express.static middleware.
  - create a middleware which works similar as express.json and express.urlencoded.
  - create a middleware that functions similar to logger and logs request url, method and host for each request

// routing
  - handle get request on '/' route with sending 'hello Express' in response.
  - handle get request on '/contact' route with an HTML contact form
  - handle POST request on '/contact' route
    - send some data as POST on '/contact' from postman
    - capture data and send it in response as res.json()

// templates
  - add view engine as ejs to the express application
  - set views directory for all ejs templates
  - add a get request on '/about' and render  'about.ejs' from views directory.
  - create a partial called 'header.ejs' and include it in multiple templates.


  