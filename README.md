# Spotify Profile

![screenshot 37](https://user-images.githubusercontent.com/8587332/51860438-ae729980-2307-11e9-9aed-628c6023c01a.png)

> A web app for visualizing personalized Spotify data

Built with a bunch of things, but to name a few:

- [Spotify Web API](https://developer.spotify.com/documentation/web-api/)
- [Create React App](https://github.com/facebook/create-react-app)
- [Express](https://expressjs.com/)
- [React Router](https://reach.tech/router)
- [Styled Components](https://www.styled-components.com/)

## Setup

1. [Register a Spotify App](https://developer.spotify.com/dashboard/applications) and add `http://localhost:8888/callback` as a Redirect URI in the app settings


## Deploying to Heroku

1. Create new heroku app

   ```bash
   heroku create app-name
   ```

2. Set Heroku environment variables

   ```bash
   heroku config:set SPOTIFY_CLIENT_ID=XXXXX
   heroku config:set SPOTIFY_CLIENT_SECRET=XXXXX
   heroku config:set REDIRECT_URI=https://app-name.herokuapp.com/callback
   heroku config:set FRONTEND_URI=https://app-name.herokuapp.com
   ```

3. Push to Heroku

   ```bash
   git push heroku master
   ```

4. Add `http://app-name.herokuapp.com/callback` as a Redirect URI in the spotify application settings

5. Once the app is live on Heroku, hitting http://app-name.herokuapp.com/login should be the same as hitting http://localhost:8888/login
