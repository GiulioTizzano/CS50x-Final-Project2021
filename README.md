# To Do List
#### Video Demo:  < https://www.youtube.com/watch?v=ual119jhRnM >
#### Description:

My 'To Do List' final project is a fairly simple flask web application following a MVC architecture pattern. The main goal of this project was to deepen my knowledge
on how the backend of a dynamic web application works rather than concentrating on frontend development. The application contains a basic layout and style from Bootstrap,
the idea behind the project is to be able to write and delete daily pending reminders of chores and tasks that have to be done. The files which make up my final project are
a static folder, templates folder, __init.py__ file, auth.py file, main.py, models.py file, views.py file and a database.db file.

Static: The static folder contains the index.js which has a javascript script which allows to add or delete text from the list.

Templates folder: The templates folder contains 'base.html' which has all the html code and jinja logic forming the 'skeleton' or 'base' of the other html files.
Then we have the 'home.html' file which
has a form tag and text area where the inputs for the to do list are written. In 'login.html' there is a form with different input fields where the user can enter their email adress
and password. Lastly 'sign_up.html' contains another form with input fields where the user will fill in their credentials in order to register.

__init__.py: Contains all registered blueprints, the name passed to the database, the __init__.py file in a directory indicates to the Python interpreter that the directory
should be treated like a Python package. When a module is imported into a script, that module's __init__.py file will be sourced and executed.

auth.py: Contains all the boolean logic for the /login and /signup routes in order to provide restrictions and security for users who register and login to the web application. Once
the user registers all of the user's information is uploaded and added into the database. When the user inputs the password into the registration form the password is hashed
using the sha256 hashing algorithm. The hash is then stored into the database rather than the inputed password itself.

models.py: Is where the database was set up using SQLalchemy. It contains the classes, objects and tables used to set up the database.

views.py: Contains all the python code which allows 'home.html' to be accessed if and only if a user is REGISTERED and LOGGED IN.

main.py:  Contains code that will run our flask app + everytime a change is made to the python code it's going to automatically rerun the web server.