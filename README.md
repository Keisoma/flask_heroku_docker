# flask_heroku_docker

## Build the image and run Docker container to make sure the app works

`docker build -t flask-heroku:latest .` builds the image with the included Dockerfile
`docker run -d -p 5000:5000 flask-heroku` runs a Docker container with the image
Open a browser tab and go on localhost:5000 to make sure you have the app working

## Deploy on Heroku

First, you have to login to Heroku using your credentials `heroku container:login`
Then, create your app on Heroku using `heroku create` 
Your app will be created with a name, that we will refer to using [appname]. </br>
You can check your Heroku apps using `heroku apps` to eventually find the name of your app

Then, you have to push and release your app using these :
`heroku container:push web --app [appname]` to run the container into the heroku repository
`heroku container:release web --app [appname]` to release on Heroku

You should now be able to find your app on heroku on the address: https://[appname].herokuapp.com/


