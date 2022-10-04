Problem:-
-> Automate the tracking of zoom attendance of a specific meeting (which is kept to recurring) to a google sheet

Solution:-
-> Took a deep look into Zoom APIs and found Zoom APIs itself provide the facility to record the attendance details of the participants.
-> Inorder to solve the above problem i used python language as it is very convenient and made for these type of tasks.
-> My program will call the Zoom APIs to fetch its participant details with the help of API_key and API_secret and then store it in gsheet with the help of gsheet credentials.
-> I used JWT API for Zoom API authentication as it is also recommended by Zoom itself and it also allows us to do server-to-server authentication and it have api keys and secret.
-> Created a gsheet folder to store all the information and codes require for acessing the google sheet.
-> In __init__.py i initialised the basic informationabout the meetings as we will fetch them often
-> In credentials.json i stored the API crediantials downloaded from Google developer APIs (it stores information like google sheet name, IDs and tokens)
-> Created a main.py file which is authorizing the user using credentials.json and converting gsheet into dataframe subsequently fetching the useful column
->->->->->
-> I created another main.py in the root folder which will work like an orchestrator as it will construct both gsheet and zoom file and use them in scripting.
-> At first i imported the needful modules and files.
   -> Fron gsheet folder i fetched the meeting ID
   -> JWT - to securely transmit information between parties as a JSON object
   -> Requests- to allow us to send HTTP requests using Python 
   -> Pandas- It will transform and simplify the data to human readable tabular form
-> In the first function i generated a token using the API_key and API_secret which i stored in the .env file
-> In get user function i retrived the participants informations with Pandas.
-> In attendance function i took the user details(attendance) and stored them a csv file

From endless possibilities i choosed to scrap details using APIs and solve the problem.
