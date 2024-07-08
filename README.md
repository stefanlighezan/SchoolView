
# SchoolView
*SchoolView uses Instructure's Canvas API across multiple devices (phone and web), to make sure you never forget your notes!*

**

# Setup

Install the [SchoolView.apk](https://github.com/stefanlighezan/SchoolView/blob/main/Android%20App/SchoolView.apk) found in the Android App directory to your Android phone (>8.0v). Then, once it is installed, we need to work on getting your access token. Head over to Canvas and get your access token from clicking "Account", then "Settings", and scrolling down to "+ New Access Token". Click on the "+ New Access Token" button, and set the purpose to any character or string, I recommend writing "SchoolView", in case you lose your token or copy the wrong part of it, it will be easy to find again. Copy the access token in its **entirety until you make sure you've reached the end of the string**. Once you have that token, find your Canvas domain name. To do this, just look at the URL of your Canvas webpage. All Canvas URLs are in the format "{canvas provider}.instructure.com/".   (Where {canvas provider} is your Canvas Provider, usually the district}. Copy that string from the website and don't forget to add "https://" to the beginning. Now you should have a string in this format: **"https://{canvas provider}.instructure.com/".** Now, here comes the very low-level string manipulation. Remember your access token that you copied a while ago? Well, now it's time to add it to our string. So to do that, we will add two things, the API, and your access token. To do the api, add "/api/v1/courses" to the end of your link. The link should now look like this:
**https://{canvas provider}.instructure.com/api/v1/courses**. The final addition to our string is the access token. We just need to add "?access_token={accessToken}", where {accessToken} is the access token you copied earlier. Our completed access token url (which you will input into the Android app) is:
**https://{canvas provider}.instructure.com/api/v1/courses?access_token={access_token}**. That's all there is to setup (unless you don't have an email address)!

# Web App
There isn't any setup to the web app except for logging in with the credentials you gave in the app. In the web app, you can organize your drafts into courses. When you click on a course, it will show you all the notes you attached to the course.  

You can find the web app [here](https://stefanlighezan.github.io/)
