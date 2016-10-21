## Phase 2 mastery guide
---
#### Do the following activities 10 times for a feedback loop that is fast.
#### If you are stuck for more than 10 - 15 mins after googling, GET HELP!
#### If the challenge is taking too long for feedback, break it down further.
#### Read other peoples code throughout the day.
#### If you know you are not getting something, schedule office hours.
#### If you think you get everything and feel that you have mastered. something, schedule office hours and prove it.


# OOJS
---
#### Create objects
- Create a object with [constructor method](https://github.com/sf-bobolinks-2016/phase-2-assessment/pull/16/files)

```js
 var Employee = function(args){
    this.firstName = args.firstName;
    this.sales = args.sales;
  };
  Employee.prototype.totalSales = function(){
    return this.sales.reduce(add,0);
  };

  function add(a,b){
    return a + b;
  };


  // to calculate average sales, calculate total sales and then divide by the total number of sales
  Employee.prototype.averageSales = function(){
    return this.totalSales() / this.sales.length;
  };
```
- Create a object with [object literal method](https://github.com/sf-bobolinks-2016/oojs-garden-challenge/pull/1/files)

```js
  var garden = {
     name: "Kula Botanical Garden",
     location: "Makawao",
     flowers: [],
     addFlower: function(flower){
       garden.flowers.push(flower)
     },

     plant: function(flower_array){
       flower_array.forEach(function(flower){
         garden.flowers.push(flower)
       })
     },

     remove: function(flower){
       garden.flowers.splice(flower)
     },

     flowersByColor: function(color){
       newArray = []
         garden.flowers.forEach(function(flower){
         if (flower.flowerColor === color){
           newArray.push(flower)
         }
       })
         return newArray
     },

     flowersByName: function(name){
       nameArray = []
         garden.flowers.forEach(function(flower){
         if (flower.flowerName === name){
           nameArray.push(flower)
         }
       })
         return nameArray
     },
   }
```
- Populate the objects with attributes
  - set all to predefined values
  - set all to passed in arguments
  - create functions that result to values
    - sum of all items
    - average of all items
    - find values of objects that were passed in
      - .name, .age, etc
  - set all attributes to results of other functions
  - set all attributes to passed in args from Jasmine specs
    - think soda machines and the objects that get passed in

# AJAX
---
#### Make a webpage reactive topics
- DOM navigation:
  - .parent()
  - .children()
  - chaining methods
- What does Ajax do and why use it?
  - what does ajax get from an erb?
- Event listeners
  - what is 'this'?
  - when to use 'this'?
  - when is 'this' mutable and why is that a problem?
- Use clean top of page listener setup calls in [application.js](https://github.com/sf-bobolinks-2016/phase-2-assessment/pull/16/files)

```js
$(document).ready(function(){
  createAddPostSubmitListener('#post_form');
  createLikePostListener('#posts');
});
```
- Event delegation
  - Why do we use it and when?
  - Create listeners 10x each for
    - links
    - buttons
    - clicks
    - form submit
  - Modify the dom 10x each to
    - Append / Prepend some text or value
    - Append / Prepend a div
    - Append / Prepend to a div
    - Append / Prepend an erb partial return
    - Send information from ajax to your ruby controller
      - parse and to_json
      - serialize
  - .ajax vs. .post / .get
    - what information is needed?
    - set needed info from the listenter as a var and use it
  - .done(function(response){
    do some things here
  })
    - What happens here?
    - What information is needed?
      - What is the 'response'?
    - set needed info from the listenter as a var and use it
  - .fail
    - how to handle errors
    - demonstrate the different ways
  - promise calls (extra credit)

# Sinatra & CRUD
---
#### Database and schema
  - Rake commands
  - Build your own rake profile
  - Do shirts!, hotels, and teams challenges
    - When to use through options
    - When to use the source and class_name options

#### Migrations
  - creating an index in the models?

#### Routes
  - RESTular and conventions should be crisp
  - Full single resource with CRUD logic app
  - Full two resource with CRUD logic app

#### Nested Routes
  - adding resources that depend on the params of the current route
  - showing resources that depend on 2 id's from params

#### User Auth
  - bCrypt in the user model
  - validations
    - username
    - password
  - sessions
  - clear the cookies for local host

#### Helpers
  - Sessions
  - Any repeaded controller functions
    - login
    - logged_in?
    - current_user
    - logout

#### Controllers
  - logic for CRUD
  - Organization of routes
    - Logical folder structure

#### Views
  - Organization of files
  - Forms vs. links
    - passing hidden methods through values
  - Params
  - Embedded ruby logic
  - Using ID's and Classes when needed
  - Basic CSS

#### Partials
  - When to use a partial?
  - When to pass locals in through the ERB's?
  - layout.erb
    - Headers and footers
    - _header.erb
    - Used if needed to show and hide certain items for user validation
  - <%= yield %> works for passing in the erb files to layout and also partials

# API's
---
#### MVP
  - Pick an api early and become familiar with the data you can get out of it
  ## DO NOT PUSH TO GITHUB BEFORE THIS STEP!!!
  - Hide your keys
    - Dotenv gem and .env file usage for all keys used in your app.


#### Research & tools
  - Postman: View the api calls in the brower before making the route
    - Parsing the json or csv or other format can take some effort.
  - Curl: The command line utility for api calls
  - Use HTTParty gem for easier API wrappers and calls as a helper module

# Deployment
---
#### Heroku
  - Once you have your git repo, depoly the hello worl app.
  - Push future commits here as well as github

#### Debugging
  - p out everything in the sinatra controller
  - console.log everything in the js files
    - alerts work too in the browser
  - debugger
  - pry
  - irb














