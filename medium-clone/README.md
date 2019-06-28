## Medium clone
Create a server side rendered application where a user should be able to add articles, view others articles, like an article, add articles as favourite, add comments on  articles.

### Application Structure
  - create an express application
  - add user login using passport-github
  - user should be able to create an article
  - user should be able to add comment on articles
  - should be able to add others article as favourite
  - should be able to follow other users

Model Structure should be..
  1. User model
    - name
    - username
    - email
    - photo
    - favourites // [Array of articleIds]
    - articles // [Array of his articles]
    - timestamps

  2. Article model
    - title
    - description
    - slug(generated from title)
    - tags // [array of strings]
    - author // ObjectId of user who created it
    - comments // [Array of ObjectIds of comment]
    - likes // Number
    - likedBy // [array of ObjectId of users who liked it]
    - timestamps

  3. Comment Model
    - description
    - author // ObjectId of User
    - articleId // ObjectId of article

*NOTE*
  - Only the author of an article should be able to edit/delete his articles, not other logged users.
  - only the author of the comment or the article should be able to edit/delete the comment.

Application will have following pages:
  1. Login Page
  2. Landing page with list of all articles sorted by latest articles.
  3. Article details page where you can read articles, like the article, favourite it or add comment to it. It should also list all the comments made on that article.
  4. tags page, where list of all the tags should be there.
  5.Clicking on particular tag should take to a list of all articles where specific tags have been used.
  6. Author page, lists all authors on webpage
  7. Clicking on author takes to list of articles created by that specific author.

