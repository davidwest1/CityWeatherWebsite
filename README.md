# <h1>City Weather Website</h1>

<h2>Description</h2>
This project consists of a website that allows the user to input a city and receive the current weather conditions for that city, utilizing a call from the OpenWeatherMap API.
<br />


<h2>Languages and Frameworks Used</h2>

- <b>Python</b>
- <b>FlaskAPI</b>


<h2>Environments and Utilities</h2>

- <b>Visual Studio Code</b>
- <b>OpenWeatherMap API</b>

<h2>Program Walk-Through:</h2>

<p align="center">
https://youtu.be/JzngBISKnXA
<img src="https://i.imgur.com/ljiWWvH.png" height="80%" width="80%" alt="City Weather Website"/>
<br />
<br />

  
<h2>Explanation Notes</h2>

Index template- houses the link to the style.css file which gives the browser webpage the gray color and white font style that is shown when the application is running. Flask uses this index template to insert the value of the “style.css” file when it is called.

City-not-found html - the same as the index html file, only this page is called when the user enters words that are not an actual city name

Weather.html - is the file which houses the layout for the response page. It shows the name of whatever city the user entered in the initial form. The user is also able to enter in another city from the response screen as well and call temperature data from as many cities as they desire.

Weather.py file - is the file which includes the call to the OpenWeatherMap API 
- load_dotenv loads the API key value from env file more specifically the os.getenv
- get_current_weather is a Python get function to request a specific portion of json data from the actual API and return a response value
- pretty print was used to present the output in a more attractable way

Server.py - the file that is ran on the web browser
- Flask is used in this page to recall the “get_current_weather” function we made in the weather.py file, which fetches a specific city’s conditions from the API
 
- Flask also uses different routes to access the numerous pages in the web application, in this case to access the home page of the API and the response page for when a weather call is made by the user. This  is shown in the /weather route seen here.
- Weather data, which is gathered from the get_current_weather function inside of the JSON file, is called from this specific page as well. ("Title", "Status", "Temp" and "Feels Like" are all data titles derived straight from the JSON file, which are also coordinated with the terms in the weather.html file). It is important to use the same terminology here so that the data can be accurately transferred.
- The .1f formats the temperature degree to only one decimal place. 

The only difficulty I faced was implementing the "city not found" screen for when the user enters words that are not a city name. Also, differentiating that path from when the user just enters spaces and then sees the default Philadelphia weather conditions, was also a bit tricky. 
