# Emaily

## Deployment

This app is using Heroku for deployment. The Heroku CLI is required.

### Initial Configuration

1. Create a Heroku account
1. Download the Heroku CLI
1. Login to the Heroku CLI by using `heroku login`
1. (DO NOT DO THIS AGAIN UNLESS NEW PROJECT) Create a new heroku app by running `heroku create`. Use the 2nd link and add it as a remote origin (below one is the one ).
1. Add remote heroku `{the 2nd link}`. The one for my app is `https://git.heroku.com/obscure-gorge-31285.git`.

### Dynamic Port Binding

The dynamic port is provided by Heroku via an enviromnent variable. For basic development work, the port is 5000.

### Specify Node Environment

We must tell Heroku what versions of Node and NPM to use. This is specified in the `package.json` file like so:

```json
"engines": {
  "node": "8.8.1",
  "npm": "5.0.3"
}
```

### Specify Start Script

We need to instruct Heroku how to start up our server. This is specified in the `package.json` file like so:

```json
"scripts": {
  "start": "node index.js"
}
```

### Deploying

To deploy, simply run `git push heroku master`. To test the deployment, run `heroku open`. `heroku logs` will print out the logs in case of any errors.
