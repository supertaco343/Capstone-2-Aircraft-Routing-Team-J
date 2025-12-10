# Capstone-2-Aircraft-Routing-Team-J
Members: Dalton Bealer, Jeremy Bell, Brenden Guillen, Joe Panthalani, Jonathan Thornton
NOTE: This project was copied to my own public repository, the only thing that has been changed from the original project is this readme file.

## Project Description  
Project given to the group by a Boeing representative.  We designed a web based interface that accepts graphs and can apply different search algorithms to said graphs.  Meant to simulate aircraft routing for Boeing airports.  

## Features
- Real time editing/creation of graphs
- Web GUI for accessing the application, available both on the same network, and hosted on a seperate network
- Full CRUD database implementation (the ability to create users/items, search items by keywords, change user permissions/item descriptions, and remove items/users) inside web GUI
- Storage of graphs and previous runs of algorithms
- User login and separate storage for graphs

## Tech Stack
**Backend**: Python, Flask  
**Frontend**: React  
**Database**: Postgresql  
**Deployment**: Web based deployment  

## Installation and Setup
1. Clone the repo:
```
git clone https://github.com/supertaco343/Capstone-2-Aircraft-Routing-Team-J.git  
cd Capstone-2-Aircraft-Routing-Team-J/backend
```
2. Install Dependencies:
```
pip install -r requirements.txt
```
3. Setup Postgres Database:  
We used a Fedora virtual machine to run and dev the project, if you are using a different version, please find the proper documentation for setting up postgresql.
The Fedora documentation can be found [here](https://docs.fedoraproject.org/en-US/quick-docs/postgresql/)
If you are using Fedora as well, you might have to change another variable, follow [this](https://www.reddit.com/r/Fedora/comments/seyvjg/anyone_able_to_properly_set_postgresql_in_fedora/) reddit post in order to change the appropriate file.  This is due to Fedora being more "locked" down than other distros.  

5. Changing ".flaskenv" file:  
Open the .flaskenv file with your choice of text editor, and add your username, password, and database name in the <> spots in that file that you created for the postgresql database.  Be sure to remove the <> parts as well.  This file may not show up on your file explorer normally, unless you ask it to "show hidden files".  

6. Starting the backend and frontend:  
Assuming you are still in the backend folder in terminal (if you are not, go there in the terminal now), run the commands below to update the database properly and start the backend:
```
flask db upgrade
flask --debug run
```
Assuming you setup the .flaskenv file correctly, this should start the backend.  Keep this terminal open while opening up a new terminal window and navigating to the frontend directory.  Once there, run the following commands:
```
npm install
npm run dev
```
This will start the frontend.  From here it should display a link for you to go to in your browser (default is http://localhost:5173).  Go to this link to access the site.  

7. Features in the web app:  
Now you should be seeing a login page, go ahead and go to the register page and add your own account name and password, if it says "Registration Failed", then look at the terminal with the backend running on it, and see what the issue could be.  If it is not seeing the database (ie, database not found), then you might have messed up the initial configuration with postgres, or entered your database name into the .flaskenv file incorrectly.  If it has an issue with the authentication, then you could have messed up the .flaskenv file again, or your linux install does not like how postgres authenticates, and you will have to search online for ways to solve this.  
If you are greeted with "Registration Successful", then proceed to login with the same credentials you just made, and it will take you to the graph import/creation screen.  Here you can import your own graph (look to the SampleGraphs folder for how your graphs should be formatted), or start to create your own graph inside the website.  After creating/uploading your graph, give your graph a title and save it (you may have to scroll down to see this portion).  Once saved, then go to "My Graphs" in the top right corner of the site, and from there you can view, edit or delete the graph.  If you click on the view tab, you can run different algorithms on that graph, and these are saved alongside that graph.  Clicking on any of the "runs" will highlight the run itself for better viewing.  
These are the main features of the project, enjoy playing with it from here!  
