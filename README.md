# JSConf.ar Live Dashboard

On the venue we setup three 60" TVs to display information about the event (like next speaker), the venue (a small map for localization) and social media (Features Tweets, YouTube, Swarm checkins).

Each TV had a notebook with a browser in kiosk mode and it connected to the server running "node server.js"

![alt tag](https://raw.githubusercontent.com/sbehrends/jsconfar-2014-dashboard/master/public/static/images/dashboard.jpg)

To deploy the dashboard just follow simple steps:

**1. Download dependencies**
```
npm install
```
**2. Customize /config.json with your own Twitter & Foursquare credentials and Youtube video id**

**3. Last but not least, run server**
```
node server.js
```

To access the dashboard locally you have three endpoints, one for each TV (we had three differents locations for the TVs with a different purpose)
 - http://localhost:5000/tv/1 - TV located downstairs on the lobby with twitter, swarm and youtube information
 - http://localhost:5000/tv/2 - Second TV on the lobby highlighting agenda and venue map
 - http://localhost:5000/tv/3 - TV located upstairs just besides the auditorium that displays agenda featuring current speaker.

Finally we had a endpoint that worked as remote for changing the current speaker at will from a staff smartphone. (http://localhost:5000/control/randomhash)

>
> We strongly recommend using "Device Mode" on Developer Tools to simulate vertical 1080x1920 TV.
>
