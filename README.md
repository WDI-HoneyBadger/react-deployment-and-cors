# React Deployment!

![](https://uploads.toptal.io/blog/image/92137/toptal-blog-image-1455717817638-f1c9424752a145ebf97219ec7a2d6cca.gif)

For this project you have been creating 2 applications. One for your front end, and one for your back end. That means twice as much fun with deployment! Here are some steps to get your app up and running on the internet. 

### 1. Seperate your applications 

Make sure your applications are in two seperate repositories. One of them containing your react application and one of them your Express API. This means that on github they should be completely seperate with git initiated in them individually and different remotes.

### 2. Deploy your API using Heroku

Refer to this guide:

- [Express Deployment](https://github.com/WDI-HoneyBadger/heroku)


### 3. Deploy your React App

We will be using [Surge](https://surge.sh/) to deploy our react applications. Its really convenient! The steps are: 

- `npm install --global surge` *(only necessary the first time)*
- `cd your-react-project`
- `npm run build`
- `cd build`
- `surge` 
- Follow the steps and you're done! Go see your app!

# CORS
Right now we're using that cool Chrome CORS widget to make sure our backend and frontend can communicate.  We can't depend on all users having the same extension.  To get around this let's enable our API to accept CORS requests.  To do this we'll be using an npm package called `cors`.

To use it:
1. Navigate to your API directory.
2. In the root directory of your API (where you see the `package.json` etc) install the package by entering `npm install --save cors` in the command line.
3. at the top of your `index.js` require the library by adding `const cors = require('cors')`
4. in your `index.js` find where you define the variable `app`.  Right below that put `app.use(cors())` and you are good to go!
