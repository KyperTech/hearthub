#Hearthub Site

This is the website code for the Heart Hub project. This project is currently under development, and therfore we can not share much about it's content. Please contact scott@kypertech.com for any questions or feedback.

Our site implements [angularjs](angularjs.org) for templating and routing. It also implements [grunt](http://gruntjs.com/) for development and deployment task management.
##Install
Note: make sure that you have [nodejs](http://nodejs.org/) and [grunt installed](http://gruntjs.com/getting-started) before starting
1. Clone the repository and cd into it
2. Install development dependencies: Run `npm install`
3. Start server and open root file in chrome: Run `grunt`

## Hosting
We currently use amazon web services s3 to statically host the client side code. There are two different buckets which serve as a production site and a test site. Using the different grunt tasks, code can be written to each bucket seperatley.

There is currently a grunt task to push to S3, but it requires that s3cmd be installed. You must also have access to the bucket which requires me entering your information in the sharing of the bucket.


####Push to Production Site
Run `grunt dist` to push currently saved code to the production website (you should always run on test server at least once first).

####Push to Test Site
Run `grunt test` to push code to test website

##Grunt Task

Grunt tasks are called by typing them after the word grunt in the command prompt. When you just type `grunt` by itself, you are running the default task, which in our case consists of connect, less, and watch.

Here is an explanation of some of the tasks:
* Watch: watches files and reloads when they are changed
* Less: Compiles less files into css file when less file saved
* Connect: Simple server to create a localhost for the site

All tasks can be called on their own, or can be run together using an alias. Our current aliases include:
* Forge
* Serve
