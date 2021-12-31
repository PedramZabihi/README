Weather Web App

Video demo: https://youtu.be/n9mqDxJzVfA

Description:

Hello CS50 people!

My name is Pedram Zabihi and I attended CS50xIran in 2021 summer.

The final project is a weather reporting app with five day forecast and it is written in Python.

The location of the user is based on their IP so entering location won`t be necessary.

The site itself is pretty simple with the location displayed on top and six sections below. First tile being today`s weather and the other five are the next five days forecast.

Each tile includes an icon representing each weather condition and a simple explanation for the weather. Extra information are temperature, humidity, wind and for the days forecast visibility (this one is not included in other tiles). Below the first tile is the time of last updated and other five have their dates.

The Python program includes multiple APIs for IP-Geolocation tools and the weather forecast itself. I have used trial or borrowed APIs so unfortunately this service won't be available for much longer.

I grabbed icons for weather conditions from [www.iconfinder.com](http://www.iconfinder.com) API and more detailed ones can be added later if necessary.

The geolocation tool is from https://main.whoisxmlapi.com

And the weather forecast is from openweathermap.org

Let's talk code:

Here's how to install requirements, the commands are given below:

\``` bash

sudo apt update

sudo apt install software-properties-common

sudo apt install python3.7

\```


\``` bash

\# With PyPi

sudo pip3.7 install -r requirements.txt

\```

and then clone this repository and run it just by typing like:

\``` bash

python3.7 application.py

this will run the Website on 0.0.0.0 at port 8585!

\#### Functions:

Let's look at application.py 

If index() : we get some information about client which where does user live by getting and analyzing IP address by **whoisxmlapi** API!

Then after getting city of that IP address, we use that to weather API (openweathermap) to get id of that city!

After these steps we are ready to get weather forecast of city\_id by again openweathermap! 

After index function as you can see there are some template filters as:

str\_datetime, date\_time and w\_icon

str\_datetime: changes UNIX time to human time(I mean Datetime!) and compare it to present time (now – some\_time)

and then return like: ? minutes ? secs

date\_time: as you can guess this filter can change UNIX time to datetime for getting upcoming days for forecasting!

And the most beautiful filter belongs to w\_icon:

Which this template filter that can show you weather climate in some cute images! As you can see in main page of  the site!



\# There is another function called countdays:

This little function can compare two datetimes and return it as minutes and seconds.

\## Template:

In template there are 2 html files which layout.html is the basic layout of the main webpage and index.html is the one which shows the weather in some separated cards view!


I couldn’t get through this course without the help of my dear friend Shayan Hallaji who has gone through it with me, so a lot of love to him.

***This was CS50***
