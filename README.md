## Phase 2 mastery guide
---
#### Do the following activities 10 times for a feedback loop that is fast.
#### If you are stuck for more than 10 - 15 mins after googling, GET HELP!
#### If the challenge is taking too long for feedback, break it down further.
#### Read other peoples code throughout the day.
#### If you know you are not getting something, schedule office hours.
#### If you think you get everything and feel that you have mastered. something, schedule office hours and prove it.

#### Questions and BOBOLINKS Cohort Wishlist:
- What is a js object in the console and what to do with it?
- Event delegation more emphasis
- JS and AR drills
- The pertest email with the examples were key for the needed core skills.
- Workflow
- Live coding examples (crud and routes perhaps in the passion project)
- Office hours were too clustered and not enough one on ones
- Review of a harder challenge from the day before in the AM
- API skills
- Heroku
- REST concepts
- Schema associations validations
- Error messages / status and handeling
- Too much time on passion project issues
- Not to keep redoing what you are strong in
- Ask for feedback on the scope and complexity of passion project


# OOJS
---
#### Create objects
- Create a object with [constructor method]
- Create a object with [object literal method]
#### Work with objects
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
  - clear the cookies for local host on window close

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
  - Hide your keys
    - Dotenv gem and .env file usage for all keys used in your app.
## DO NOT PUSH TO GITHUB BEFORE THIS STEP!!!

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
    - git push heroku master && heroku run rake db:migrate && heroku restart

#### Debugging
  - p out everything in the sinatra controller
  - console.log everything in the js files
    - alerts work too in the browser
  - debugger
  - pry
  - irb


