# Home Jungle
This is an e-commerce website for selling plants and plant decoration. 
The website will be a site where users can browse through plants and plant decoration and will be able to purchase them. 

_This app is made for educational use only._

## Deployed Site
[Live website](https://home-jungle.herokuapp.com/)

## Index
- [UX](#ux)
  - [User Stories](#user-stories)
  - [Strategy](#strategy)
  - [Scope](#scope)
  - [Structure](#structure)
  - [Code Structure](#code-structure)
  - [Skeleton](#skeleton)
  - [Surface](#surface)
  - [Mockups](#mockups)
- [Features](#features)
  - [Database Schema](#database-schema)
  - [Features left to implement](#features-left-to-implement)
- [Technologies](#technologies)
  - [Deployment](#deployment)
  - [Setting up Heroku](#setting-up-heroku)
  - [Deploying to Heroku](#deploying-to-heroku)
  - [Committing files to GitHub](#committing-files-to-github)
- [Credits](#credits)
  - [Content](#content)
  - [Media](#media)
  - [Acknowledge](#acknowledge)

## UX

### User Stories

Viewing and Navigation by Shopper
- View a list of all the products
- View individual product details
- Quickly identify different type of products
- See the total amount in my shopping bag

Registration and User Accounts by Site User
- Easily register for an account
- Receive an email confirmation after registering
- Easily login or logout
- Easily recover my password
- Have a personalized user profile

Sorting and Searching by shopper
- Sort the list of available products
- Sort a specific category of products
- Sort multiple categories of products simultaneously
- Search for a product by name or description
- Easily see what i’ve searched for and the number of results

Purchasing an Checkout by shopper
- Easily select the quantity of a product when purchasing it
- View items in my bag to be purchased
- Adjust the quantity of individual items in my bag
- Easily enter my payment information
- View an order confirmation after checkout
- Receive an email confirmation after checking out

Admin and Store Management by store owner
- Add a new product
- Edit a product
- Delete a product

### Strategy

This website is designed so users can scroll throught the products and sort them in several ways. By clicking on a product they can read the product details and add the product to their shopping cart. When a product is added, the user can click checkout to complete their order by filling in the form. <br>
Every user has the option to register for an account and to login at their account. <br>
On this website the admin has the option to use all the CRUD functions: Create, Read, Update and Delete.

### Scope
All the necessary files are together in the following folders:
- bag = for The Bag Page: for users to see what is in their bag
- checkout = for The Checkout Pages with all the information before and after placing the order
- home = for The Home Page: the landing page where users can select how to view the products
- home_jungle = the Python code for this website
- media = all the images used on the website
- products = for:
  - The Products Page: a page with all the products, sorted by the way the user has choosen
  - The Product Detail Page: to view each product with more details
- profiles = for The Profile Page: with all the personal information and order history of registered users
- templates = for:
  - The Base Page: with the whole navbar
  - The Navbar Pages: for displaying the navbar depending on the screen size
  - The Toasts: the pop-ups with extra information
  - The Allauth Pages: for all logging options
- static: all the static files
- readme: all the extra files for the README

### Structure
- Header: 
  - On the top a autoplay slider with messages
  - Navbar on large devices:
    - Top-navbar with on the left the title, in the middle the searchbar and on the right the menu items (My Jungle & Shopping Cart)
      - The My Jungle dropdown menu will change, depending on if the user is logged out, loggin in or it’s the admin
      - The Shopping Cart will change, depending on if the Bag is empty or filled
    - Main-navbar with the menu categories
  - Navbar on medium and small devices:
    - Hamburger icon with dropdown menu: home and categories
      - Each category has it's own dropdown menu
    - Search Icon that will search trought all the products
    - My Jungle icon with dropdown menu that will change, depending on if the user is logged out, loggin in or it’s the admin
    - Shopping Cart icon
- Landing Page: very large button to go to all the products
- Login Page: form field with buttons and checkbox
- Signup Page: form field with buttons
- Profile Page: form field with buttons + order history
- Add Product Page: form field
- Edit Product Page: form field with checkbox
- Bag Page: button + added product
- Logout Page: buttons
- Password Reset Page: form field with buttons
- Checkout Page: buttons
- Products Page: all products
- Product Page: product details

### Code Structure
![Part 1](readme/codestructure_bag_checkout.JPG)
![Part 2](readme/codestructure_home_products.JPG)
![Part 3](readme/codestructure_profiles_templates.JPG)
![Part 4](readme/codestructure_readme.JPG)

### Skeleton 
- Header: 
  - Top Slider:
    - Message 1: New plants coming soon!
    - Message 2: Free delivery on order over $50!
    - Message 3: Deliveries can take a bit longer than usual.
  - Top Nav:
    - Title: link to homepage
    - Searchbar: searches trought all products
    - My Jungle:
      - User Icon
      - Dropdown Menu:
        - Logged out user:
          - Register
          - Login
        - Logged in user:
          - My Profile
          - Logout
        - Logged in admin:
          - Product Management
          - My Profile
          - Logout
     - Shopping Cart:
        - Basket Icon
  - Main Nav Menu: 
    - All Products is a collapsible menu with four options:
      - By Price
      - By Rating
      - By Category
      - All Products
    - Plants is a collapsible menu ton with four options:
      - Africa
      - Asia
      - America
      - All Plants
    - Pots is a collapsible menu with three options:
      - Indoor
      - Outdoor
      - All Pots
    - Decoration is a collapsible menu with three options:
      - Pillows
      - Other
      - All Decorations
- Homepage: 
  - Button 1: link to product page
- Signup: form field:
  - Field 1: e-mail address
  - Field 2: e-mail address confirmation
  - Field 3: username
  - Field 4: password
  - Field 5: password confirmation
  - Button 1: back to login
  - Button 2: sign up
- Login: form field:
  - Field 1: e-mail address
  - Field 2: password
  - Checkbox: remember me
  - Button 1: home
  - Button 2: sign in
- Password Reset: form field:
  - Field 1: e-mail address
  - Button 1: back to login
  - Button 2: reset my password 
- Logout: 
  - Button 1: cancel
  - Button 2: sign out
- Profile: form field and overview order history:
  - Field 1: phone number
  - Field 2: street address 1
  - Field 3: street address 2
  - Field 4: town or city
  - Field 5: country, state or locality
  - Field 6: postal code
  - Field 7: country dropdown menu (all the countries included)
  - Button: update information
- Add Product: form field:
  - Field 1: category dropdown menu (Africa, Asia, America, Indoor, Outdoor, Pillows, Other)
  - Field 2: sku
  - Field 3: product name
  - Field 4 (big text field): product description
  - Field 5: sizes dropdown menu (No, Yes, Unknown)
  - Field 6: rating
  - Field 7: image url
  - Button 1: select image
  - Button 2: cancel
  - Button 3: add product
- Edit Product: form field, the same as add product. Extra option:
  - Checkbox: remove image
- Confirm E-mail:
  - Button: Confirm
- Toasts to display messages as pop ups on every page using django messages module, with messages for most actions across the website.

### Surface

- Font Family standard text: Lato
- Font Family titles and categories: Abril Fatface from Google Fonts
- Background color: white, accept the Home Page has a full image
- Color schema: green

![Dark_Green](readme/dark_green.JPG) <br>
![Light_Green](readme/light_green.JPG) <br>
![Btn_Success](readme/btn-success.JPG)

- Header slider: 
  - Text color: white
  - Background color: 
    - Slider 1: dark green 
    - Slider 2: black
    - Slider 3: dark green
- Header top-navbar on large devices: 
  - Text color: black
  - Text color inside searchbar: light grey
  - Background color: white
  - Icons: black
- Header top-navbar and main-navbar on medium and small devices: 
  - Text color: black
  - Text color inside searchbar: light grey
  - Background color: white
  - Icons color: black
- Header main-navbar: 
  - Text color: black
  - Text color inside searchbar: light grey
  - Background color collapsible product menu: light green
  - Background color collapsible Search and My Jungle icons: white 
  - Icons color: black
    - Shopping Cart Icon when filled: green
- Home Page:
  - Full page image
  - Button: dark green, white border, white text
  - Button hoover over: light green, white border, black text
- Sign Up Page:
  - Background: white
  - Title: dark green
  - Form: black borders, light grey text
  - Button 1: white with black border, black text
  - Button 2: green with black border, white text
- Login Page:
  - Background: white
  - Title: dark green
  - Form: white with black borders, light grey text
  - Checkbox: unchecked
  - Button 1: white with black border, black text
  - Button 2: green with black border, white text
- Profile Page:
  - Background: white
  - Title: dark green
  - Form: white with black borders, light grey text
  - Button: green with black border, white text
- Logout Page:
  - Background: white
  - Title: dark green
  - Text: dark grey
  - Button 1: white with black border, black text
  - Button 2: green with black border, white text
- Password Reset Page:
  - Background: white
  - Title: dark green
  - Text: dark grey
  - Form: white with black borders, light grey text
  - Button 1: white with black border, black text
  - Button 2: green with black border, white text
- Bag Page:
  - Background: white
  - Title: dark green
  - Text: dark grey
  - Button: green with black border, white text
- Add Product Page:
  - Background: white
  - Form: white with black borders, light grey text
  - Button 1: black, white text
  - Button 2: white with black border, black text
  - Button 3: green with black border, white text
- Edit Product Page:
  - Background: white
  - Form: white with black borders, light grey text
  - Checkbox: red, unchecked
  - Button 1: black, white text
  - Button 2: white with black border, black text
  - Button 3: green with black border, white text 
- Products Page:
  - Background: white
  - Images: black border
  - Sort menu: white with black border, grey text
  - Back to top icon: white with green border and arrow
  - Product: image, dark green title, dark grey price, grey tag and rating
  - Light grey horizontal border between the products
- Product Detail Page:
  - Background: white
  - Image: big with black border, aligned whole left site on larger devices, aligned on top on smaller devices
  - Title: dark green
  - Price: $ in dark grey
  - Tag: grey
  - Rating: grey
  - Product information: grey
  - Quantity: left the minus icon, middle the quantity, right the plus icon
  - Button 1: white with black border, black text
  - Button 2: green, white text
- Checkout Page:
    - Background: white
    - Form: white with black borders, light grey text
    - Button 1: white with black border, black text
    - Button 2: green, white text
    - Order Summary with the products added to the bag:
        - Product Image
        - Product text: dark grey
        - Product value: black
- Checkout Success Page
    - Background: white
    - Title: dark green
    - Text: dark grey
    - Button: green, white text
- Confirm Email Page:
    - Background: white
    - Title: dark green
    - Text: light grey
    - Button: green

### Mockups 
The following wireframes were created using Balsamiq to design the website layout options:<br>
![Homepage](readme/homepage.JPG)<br>
![Products](readme/products.JPG)<br>
![Product Details](readme/product_details.JPG)<br>
![Bag](readme/bag.JPG)<br>
![Checkout](readme/checkout.JPG)<br>
![Add Product](readme/add_product.JPG)<br>
![Edit Product](readme/edit_product.JPG)<br>
![Signup](readme/signup.JPG)
![Login](readme/login.JPG)<br>
![Logout](readme/logout.JPG)
![Profile](readme/profile.JPG)<br>
![Password Reset](readme/password_reset.JPG)<br>
![Checkout Success](readme/checkout_success.JPG)<br>
![Confirm Email](readme/confirm_email1.JPG)<br>
![Confirm Email](readme/confirm-email2.JPG)
         
## Features
The webpage consists of the following features:
- Header
  - Autoplay slider
  - The title is a link to the Home Page
  - The search bar, searches through all the products
  - My Jungle icon is a collapsible menu with multiple options, depending on the user is logged out, logged in or the admin
    - Logged out user:
      - Register will lead to the Sign Up Page 
      - Login will lead to the Login Page 
    - Logged in user:
      - Profile will lead to the Sign Up Page
      - Logout will lead to the Logout Page
    - Admin:
      - Product Management will lead to the Add Product Page
      - Profile will lead to the Profile Page
      - Logout will lead to Logout Page
   - The Shopping Cart icon will lead to the Bag Page 
  - Product Navbar will lead to the Product Page, sorted by the way the user selected  
- Home Page 
  - The button is a link to an overview of all the products     
- Products Page
  - In the right top a collapsible menu to sort the products
  - 1, 2, 3 or 4 products horizontal alligned, depending on device size
  - The Admin has the option to edit or delete the product
- Product Detail Page:
  - Option to ascend or descend the quantity of the product
  - A Continue Shopping button, which will lead to the Product Page
  - A add to Bag button:
    - Will lead to the Confirm-Email Page
    - Toast will appear with: 
      - The message: Success! Added (product name) to your bag
      - When the order total is underneath the $50,- a message will show up with how much more to spend to get free delivery
      - A Go to secure checkout button, which will lead to the Bag page
    - For the admin:
      - Option to edit or delete the product
      - Edit link will lead to the Edit Product Page
      - Delete link:
        - Product will deleted from the database
        - Toast will appear with the message: Success! Product deleted!
        - Admin will be directed to the Product Page
- Bag Page:
  - Option to ascend or descend the quantity of the product with an option to update the bag or delete the product
  - Continue Shopping button which will lead to the Product Page
  - Secure Checkout button which will lead to the Checkout Page
- Checkout Page:
  - A form with fields for the personal details, the delivery details and the creditcard number, which are all required
  - A link to Create an account, which will link to the Sign Up Page
  - A link to Login, which will link to the Login Page
  - An overview with all the products in the bag
  - An Adjust Bag Button, which will lead to the Bag Page
  - A Complete Order button, which will lead ......
- Checkout Success Page:
  - Overview of the order
  - A Back to the Shop button, which will lead to the Product Page
  - Toast will appear with the message: Success! Order successfully processed! Your order number is (order number) A confirmation email will be sent to (e-mail address)
- Sign Up Page:
  - A form with required fields
  - A link to the Login Page
  - A Back to Login button, which will lead to the Login Page
  - A Sign Up Button, when pressed:
    - The form will give an error when a field is filled in incorrect
    - Will lead to the Confirm Email Page
    - Toast will appear with the message: Alert! Confirmation e-mail sent to (e-mail address)
- Confirm Email Page:
  - A page with text to go to your E-mail provider
  - In Email provider click the link to confirm e-mail address
  - Will lead to the Confirm Email Page now with Button to Confirm
  - Confirm button will lead to the Login Page
  - Toast will appear with the message: Success! You have confirmed (e-mail address).
- Login Page
  - A link to the Signup Page
  - A form with required fields
  - A checkbox the remember the information in the required fields
  - A Home button, which will lead to the Home Page
  - A Sign In button, when pressed:
    - The form will give an error when a field is filled in incorrect
    - Will lead to the Home Page
    - Toast will appear with the message: Success! Successfully signed in as (username)
  - A link to the Password Reset Page 
- Profile Page:
  - A form with all the user details
  - An Update Information button to add/edit the form information
  - The order history
- The Logout Page: 
   - A Cancel button, which will lead to the Home Page
   - A Sign Out button, which will lead to the Home Page
   - Toast will appear with the message: Success! You have signed out.
- Add Product Page by admin:
  - Category is a collabsible menu
  - The form fields are required
  - A Select Image button will pop-up the users explorer to select an image
  - A Cancel button will lead to the Products Page
  - A Add Product button will send the new product to the database and will lead the admin to the Product Detail Page of the added product
  - Toast will appear with the message: Success! Successfully added product!
- Edit Product Page by admin:
  - Category is a collabsible menu
  - The form fields are required
  - A Checkbox to remove the image
  - A Select Image button will pop-up the users explorer to select an image
  - A Cancel button will lead to the Products Page
  - A Update Product button will send the edited product to the database and will lead the admin to the Product Detail Page of the edited product
  - Toast will appear with the message: Success! Successfully updated product!

### Features left to implement
- Social account login (Google and Facebook). This feature allows users to login using social networks accounts, Google and Facebook, that would enhance user experience and make the login process easier. And a button to share a product on their social media account.
- A place where the registered user can rate a product.
- A page where the admin can start a blog.
- A button to sign up to the newsletter.

## Technologies
- __HTML5__ was used as the main language for the templates
- __CSS__ was ued for styling the webpage
- __JavaScript__ was used for some front end functionality
- __Python3__ was used for backend data manipulation
- __Github__ was used for version control
- __Gitpod__ to build the website
- __Django__ was used as as a python based web framework
- __Django Allauth__ for the authentication system 
- __Django Countries__ which was used for the country field for user to be able to selct the contry they are from
- __Django Crispy__ Forms to helps to manage the forms and able adjust forms properties in the backend
- __Gunicorn__ (‘Green Unicorn’) is a pure-Python WSGI server for UNIX
- __Pillow__ to be able to use the image field for the products on the site
- __Stripe__ to set up the payment methods for the site as customer can pay by card
- __Bootstrap__ for responsive simplistic layouts
- __JQuery__ for the JavaScript in the website
- __Font Awesome__ to add the icons used in the site
- __Amazon AWS__ for storing media and static files for use on my Heroku site
- __Autopep8__ to tidy up my python code
- __SQLite 3__ for the database which stores the information from my site e.g. products, users
- __W3C Markup__ was used this to check my HTML for errors and typos
- __W3C CSS__ was used to check the validity of my CSS
- __Google Chrome Developer Tools__ for testing different divice sizes
- __Responsinator__ for testing different divice sizes
- __Fontawesome__ was used for some icons on the website

### Deployment
This project was developed using the GitPod and was committed to git and pushed to GitHub using the built in function within GitPod. 

### Deploying to Heroku
The app is currently being deployed on Heroku using the master branch on Github.
These are the steps that were taken to deploy to Heroku:

1. In GitHub create a requirements.txt file for Heroku can install the necessary dependencies to run the app. The command used to create the file: pip3 freeze --local > requirements.txt
2. In GitHub create a Procfile for Heroku to tell what kind of application it is deploying and how to run. The command used to create the file: echo web: python run.py > Procfile
3. Create a free Heroku account
4. Create a new app for the project, selecting a name for the app and choose the closest region
5. In the Deploy tab choose deployment method GitHub, select your GitHub project
6. In the Settings tab choose Reveal Config Vars and export the same values to GitPod
7. In the Deploy tab choose Enable Automatic Deploys
8. Open app.
