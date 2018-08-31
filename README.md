 Goal : Create custom Spotify Playlist
 
 How?? 
       > You can search by singer
       > Sort by Dancebility, Instrumentalness and Energy
       > Save to your Spotify 
       > You can reach that playlist and play from your Spotify app.
       
 Spotify OAuth v      
 
 OAuth bridge template

This service logs in to Spotify and redirects the user to a given frontend application with a valid access_token as a parameter in the url.

>  Development mode

In development mode, it assumes you are running the frontend on localhost:3000, but the server itself will be running on localhost:8888.

In order to start developing, register a Spotify Application here:
https://developer.spotify.com/my-applications

On that page, add http://localhost:8888 as a callback url (don't forget to hit save at the bottom of the page)

Write the below commands in your terminal (replacing XXXX AND YYYY with your acutal client id and secret from the page where you registered your application)

```
export SPOTIFY_CLIENT_ID="your client ID"
export SPOTIFY_CLIENT_SECRET="your client secret"
npm start
```

Then go to http://localhost:8888/login in your browser. This will initiate the login flow and finally redirect to http://localhost:3000?access_token=ZZZZZ where ZZZZZ is a valid access token that you can use to do operations in the Spotify API.

