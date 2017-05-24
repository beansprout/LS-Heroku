# LS-Heroku

### Topics
* Heroku
* npm run build
* process.env.PORT
* path
* __dirname
* /build

### Instructions

Create a folder for your full-stack application.
[x] Run `create-react-app client` to generate a react application in a `/client` folder.
[x] Run `npm init` to generate a `package.json` file.  Install `express` and `path`.
[x] Create a server file: `server.js`.
[x] Create a server that listens on port `process.env.PORT` or `8080`.

[x] Run `npm run build` inside of `/client` to generate the `/build` directory.

[x] Remove `/build` from `/client/.gitignore`.

[x] At the home route on your server `/` serve up the client application.

The following code will make the static files available on your server and will setup your home route.
```
app.use(express.static(path.join(__dirname, 'client/build')));

app.get('/', (req, res) => {
  res.status(200).sendFile(path.join(__dirname + 'client/build/index.html'));
});
```

Once you are able to serve the React application locally then you will next host the application on Heroku.

[x] Create an account on Heroku.  Use GitHub to sign up so that Heroku can access your GitHub repos.
Once you create an account specify that Node.js is the primary language you'll be using and specify the server region closest to you.
[x] Create a GitHub repo for your local server directory.  Push your code up.
    => https://github.com/beansprout/heroku-react-app

Create a new Heroku Node application and link it with your GitHub repo for your server.
[x] Go to the specified URL and test that it properly serves up the client application.
    => https://desolate-stream-96068.herokuapp.com/

