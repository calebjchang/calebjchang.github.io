---
layout: essay
type: essay
title: "Assignment3 Checkpoint"
# All dates must be YYYY-MM-DD format!
date: 2023-04-27
published: true
labels:
  - Assignment3
--- 

### Show what each page will look like.

### Describe your design for your site’s shopping cart. That is, will it be a separate page that the user can view and edit, or will it be integrated into the product pages? If so, describe in detail how this will work on your site. Provide several examples of using the cart.
I wasn't sure which way I wanted to go, but I felt that if I had the cart display on the product pages, I had to make it functional and still have a separate shopping cart page on top of that, so I will most likely opt to just have a shopping cart page. I'll have a little cart icon display in the top right, in line with my nav bar, and when a user adds a product to the cart, I want to have some kind of feedback display on the page, showing that you have x amount of items in the cart, through a message that displays or a small number near the icon. When a user adds an item to their cart, the button will create a new key-value pair in the user's session.

On the shopping cart page, I want the following functionalities to be implemented: editing item amounts (adding more, removing), the subtotal and total displays, a complete purchase button that pages to the invoice, and images for each product in the cart. For the editing item amounts, I'll put an input for each product and have two buttons below, one to complete their purchase, and one to update their cart. I also want the users to be able to access the cart whether or not they are logged in, but only be able to go to the invoice if they are logged in.


### Explain specifically how you will use sessions to manage your shopping cart. In particular, what shopping cart data will be stored in the session, what data format will be used (NOT what data type, but the format like with the data format used for your registration data). Use code examples showing what data structures (such as arrays and their objects) you will use to manage the shopping cart data and how they will be used in a session.
I am going to use sessions to manage the cart information and my current plan is to store the quantity selected/purchased in the session and have the product information stored in the server. This way, when the cart displays the items that were selected, it takes the quantity selected from the session and uses that with the products data it loads from the server to display the items in the cart. Although this may not be the best way to do this, I think this way will allow me to use my Assignment2 code without changing too much.

### How will you avoid access to your application when the user has not logged in or registered? What are the particular security concerns you must address?
The main security measures I have to address are disallowing users to see their invoice if not logged in, and logging out users after a certain amount of time. I'll do the first through a simple if-else statement to check the cookies to see whether or not they are logged in, if they are, then path to invoice, else, redirected to login. For the logging out part, I'll have the cookies expire after a set amount of time from the time from their login.

### Upon a successful login, how do you provide personalization in your UI? Explain how you did or will do this (paste code if necessary)
I will provide personalization in a very simple way; upon successful login, I'll have the user's name display in the top left corner. My nav bar is centered, and I plan to have a shopping cart icon display in the top right, so it works out well. I'll most likely have it display "hi <name>!" as it kinda fits with my website's theme. Also, if they had a cart from a previous visit, I'll have the cart display a number of items in a small number or a message that says "you have x items in your cart," it depends on which looks better. I am going to achieve all of this by using the user's cookie and session info.

### If you are working with partners, how will you split up the work in your team so that you are working in parallel as effectively as possible? That is, who is doing what and when?
I am working alone.

### How are you approaching Assignment 3 differently than Assignment 2?
I am approaching Assignment3 with a fairly similar approach, as I am building upon my Assignment2 code, but I want to change two important things in my process. Before I add anything in my backend, I want to have all my pages created with the new objects that I want to add, so that I already have my paths set up it's more of a matter of adjusting the routes in my server.js and making tweaks to my pages. 
