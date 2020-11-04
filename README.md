# Exercise-Tracker-WebApp

To create the initial structure of this application I followed this tutorial:

https://medium.com/@beaucarnes/learn-the-mern-stack-by-building-an-exercise-tracker-mern-tutorial-59c13c1237a1

I added some functionality in a “Delete Users” tab which was aimed at being only accessible via JWT for users who
had admin access. However, after running out of time, I simply left the feature available to all users.

a. The basic functionality of this app:

This app can be used to log details of users and the exercises these users perform.
Specifically the user can:

1. Create an exercise log
2. Delete or edit one of the logged exercises
3. Create a new user
4. Delete users

b. Running this application on your device:

1. Clone this Git repository to a folder on your device.

2. Access the files via an IDE or programming interface of your choice

3. Install the following:

Node JS as follows here:
https://nodejs.org/en/download/

In the backend folder:

$ npm install express cors mongoose dotenv
$ npm install -g nodemon

In the root folder:

$ npm install bootstrap react-router-dom react-datepicker axios

4. Create a Mungo DB Atlas account. The steps to create and connect to a database on Mongo, can be
seen here under the section, “MongoDB Atlas:
https://medium.com/@beaucarnes/learn-the-mern-stack-by-building-an-exercise-tracker-mern-tutorial-59c13
c1237a1

Use the connection URL (as well as your unique password and username) to replace the existing URL in
the .env file found in the backend.

5. Depending on whether you wish to deploy the app or run it locally you’ll need to update the Axios API
endpoints found under the components folder in the frontend.

For example, the code required to connect to a my production server currently looks like this:
axios.post('/users/add', user)

The above code is made to fit our production website. Should you wish to connect to a localhost on your
device, you’d need to update the code as follows:

axios.post('http://localhost:5000/users/add', user)

In the above example, this endpoint connects to localhost5000.

6. Should the above have been completed, simply enter:

npm start

And the app should be good to go on your local device!

c. Deployment:

This app was deployed using Heroku.

One difficulty I encountered with Heroku was connecting via URI to the Mongo DB database. Heroku has
built-in functionality to add this connection however, I struggled to make use of it effectively.

Instead I simply kept the .env file used to connect locally, as a commit to production. I understand doing so
is normally bad practice, however I had limited time to complete this project.

The following tutorials were very useful in re-structuring the project in order to ensure it could be deployed
successfully:

https://daveceddia.com/deploy-react-express-app-heroku/
https://medium.com/better-programming/how-to-deploy-your-react-app-to-heroku-aedc28b218ae

d. The deployed app, please feel welcome to test it out:

https://exercisetracker24.herokuapp.com/
