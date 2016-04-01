# Meteor Todo App

A simple app created by following the Meteor [getting started tutorial](https://www.meteor.com/tutorials/blaze/creating-an-app).

## Running the App

To run the app, use:

```
meteor npm install
meteor
```

And then open your web browser at `http://localhost:3000`.

### Installing Meteor

To install the latest official Meteor release from your terminal: 

```
curl https://install.meteor.com/ | sh
```

## Deploying with Heroku

Firstly you'll need to install the [Heroku toolbelt](https://toolbelt.heroku.com/) and [sign up to Heroku](https://www.heroku.com). 

Then create an app on Heroku with any name, e.g. `your-app-name`.

While in the project repository root, notify heroku of your new app using:

```
heroku git:remote -a your-app-name
```

### Setup the Heroku App

Let Heroku know that the application you're deploying is a Meteor app using the [Meteor Heroku Buildpack](https://devcenter.heroku.com/articles/buildpacks). 

```
heroku buildpacks:set https://github.com/AdmitHub/meteor-buildpack-horse.git
```

You will also need to add the MongoLab Addon to the application:

```
heroku addons:create mongolab
```

Lastly, set the project `ROOT_URL`, setting `your-app-name` to be the same as your chosen app name.

```
heroku config:set ROOT_URL=https://your-app-name.herokuapp.com
```

### Deploying

You can then simply deploy by pushing to the `heroku` remote.

```
git push heroku master
```