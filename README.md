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

#### Implementation

The frontend was build with HTML, CSS, JavaScript and the Bootstrap framework.

Flask was used in the backend of the application to implement its funtionalities:

- user registration and login
- habits *CRUD* - create, read, update and delete
- track progress of the week

To access the funtionalities of the app, the user must be registered and logged in. To ensure that, Flask Sessions was used.

The database used was SQLite, with the SQLAlchemy library.

There are three tables in the database: user, habit and checkbox. The last one is updated dinamically using JavaScript POST requests to keep track of the habits checkboxes.

##### Video demo:

*My name is Luana, and this was my final project for CS50!*
