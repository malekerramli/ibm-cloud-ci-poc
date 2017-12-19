
Getting Started
------------
the following Node.js tutorial shows the concept of deploying an application to the IBM cloud, follow the steps and you'll have a fully integrated application on the cloud.  

Pre-requisites: 
 * IBM cloud account.
 * Cloud Foundry CLI.
 * GIT.
 * Node.
 
## Step 1 : clone the sample app.
clone the nodeJs app from github 

```
git clone https://github.com/malekerramli/ibm-cloud-ci-poc
```
## Step 2 : run the app locally.
Use the npm package manager to install dependencies and run your app.
  * cd into the cloned directory  ``$ cd ibm-cloud-ci-poc``
  * install the dependencies via the package manager ``$ npm install``
  * run the app  ``$ npm start``

 
 ## Step 3 : prepare the app for deployment.
To deploy to IBM Cloud, it can be helpful to set up a manifest.yml file. 
The manifest.yml includes basic information about your app, such as the name, 
how much memory to allocate for each instance and the route. 
A sample manifest.yml file is provided in the root directory.
 
 ## Step 4 : deploy the app.
 
 ## Step 5 : add a database.
 
 ## Step 6 : use the database
 

 

Special Thanks
--------------------
- [Middleman](https://github.com/middleman/middleman)
- [jquery.tocify.js](https://github.com/gfranko/jquery.tocify.js)
- [middleman-syntax](https://github.com/middleman/middleman-syntax)
- [middleman-gh-pages](https://github.com/edgecase/middleman-gh-pages)
- [Font Awesome](http://fortawesome.github.io/Font-Awesome/)
