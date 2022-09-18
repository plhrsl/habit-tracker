# [HBT tracker](https://hbt-tracker.herokuapp.com)

This is a simple website made as the final project for CS50. Its purpouse is to weekly keep track of habits.

It was deployed using Heroku, so you can access the app in [here](https://hbt-tracker.herokuapp.com).

### Technologies

- HTML, CSS and Javascript with Bootstrap
- Pyhton with Flask
- SQLite

### Details

#### Usage 

To use the app the first step is to create an account and log in. Once logged in, the user can start adding habits by giving a name and its frequency. In the home page the user can keep weekly track of their habits, by checking when concluded on that particular day of the week. It is also possible to edit and delete existing habits.

#### Implementation overview

The frontend was build with HTML, CSS, JavaScript and the Bootstrap framework.

Flask was used in the backend of the application to implement its funtionalities:

- user registration and login
- habits *CRUD* - create, read, update and delete
- track progress of the week

To access the funtionalities of the app, the user must be registered and logged in. To ensure that, Flask sessions was used.

The database used was SQLite, with the SQLAlchemy library.

There are three tables in the database: user, habit and checkbox. The last one is updated dinamically using JavaScript POST requests to keep track of the habits checkboxes.

#### Going through the files

- templates folder

  This folder contains every `html` file of the application, such as the `base.html` - that is the base template for all pages.

- static folder

  This folder contains: 

  - `styles.css` - which is really short, given that virtually all stylization was done through Bootstrap classes.
  - `script.js` - which dynamically sends POST requests every time there is a change in one of the checkboxes of habits or the "clear" button is clicked. It also highlights the current day of the week in the homepage table and calculates the current percentage of the progress bar.
  - assets folder - where is the `logo.png`
  
 - `app.py`
 
   This is the main file of the application, in which all of the website funtionalities is implemented.
   
   This file also defines the database - `habit_tracker.db` -, as well as its tables - user, habit and checkbox -, through SQLAlchemy's object-relational mapping.
   
   The routes determine the functioning of each of the pages through Python functions. The routes of this app are:
   
   - `"/register"`, `"/login"` and `"/logout"`: which, respectively, inserts new users into the database, starts a new session if the user has provided valid credentials, and ends the session.
   
   - `"/new-habit"`, `"/habits"`, `"/edit"` and `"/delete"`: which, respectively, inserts new habits into the database, returns the already existing habits of the logged user, updates and deletes especifics habits given its id.
   
   - `"/"`: thats the `index.html` route, in which a table with the habits and checkboxes in the days of the week corresponding to its frequency is displayed. For that, the route needs to return data from the checkbox and habit tables corresponding to the user of the current session. In addition, the logged in user's name and the current date are also provided as parameters.

##### Video demo: https://youtu.be/_cSq8iq5VMQ

*My name is Luana, and this was my final project for CS50!*
