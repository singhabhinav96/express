### Shopping Cart

#### Appilcation Story

Create a shooping cart where users can login and checkout shopping items on the website.
Even anyone, without logging in can also checkout items on our website, but he should not be able to add items as favoutite or to the cart. An admin can login and add items in the shopping list of items, edit them, delete them and modify them anytime they want.

#### Admin Story
  - admin should be able to login using localStrategy or email/password login.
  - show admin dashboard with all items based on category
  - admin should be able to add items, edit their price and quantity, delete them
  - should be able to see a list of all users who have registered on shopping cart applicatiom.
  - should be able to block any user from using the site.

#### User Story
  - login user using google strategy
  - should be able to update his profile information
  - can add shopping items to their cart
  - can filter product using category and price and latest filter
  - can remove items from his cart
  - can add items as favourites
  - should be able to delete his account

### Application Structure
  - create an express application
  - use sessions/cookies for tracking user and admin sessions
  - You may need these models
    1. User Model(login using google)
      - email
      - name
      - photo
      - isBlocked / type: Boolean // default: false
      - cartId: _id of cart
      - favourites: [favourite products array]
    
    2. Admin Model(email/username, password login)
      - username/email
      - password
      - name
      - image // use multer to upload image

    3. Product Model
      - name
      - category // type Enum
      - quantity // Number
      - price //number
      - description
      - tags [array of string]

    4. Item Model
      - productId(ObjectId of product)
      - quantity(Number of quantity)

    5. Cart model(Each user should have 1 cart)
      - user // ObjectId of User
      - items (array of all items which is added by the user)[array of ObjectId of Items]


### Application Flow
  - As soon as user registers, there should be a cart created for that user.
  
  - when a user adds a product to cart
    1. create an item using product id and number of product he/she is buying.
    2. Add item to users cart

  - when a user removes item from a cart
    1. delete that item and remove it from user's cart.

  - when a user adds a product as favourite
    - add product's id into users favourite array  
