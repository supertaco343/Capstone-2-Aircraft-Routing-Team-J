# Capstone-2-Aircraft-Routing-Team-J
NOTE: This project was copied to my own public repository, the only thing that has been changed from the original project is this readme file.

## Project Description  
Project given to the group by a Boeing representative.  We designed a web based interface that accepts graphs and can apply different search algorithms to said graphs.  Meant to simulate aircraft routing

## Features
- Real time editing/creation of graphs
- Web GUI for accessing the application, available both on the same network, and hosted on a seperate network
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
Open the .flaskenv file with your choice of text editor, and add your username, password, and database name in the <> spots in that file that you created for the postgresql database.  Be sure to remove the <> parts as well.

6. CONTINUE
