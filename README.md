
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
You can use the Cloud Foundry CLI to deploy apps to IBM Cloud.
Run the following command to set your API endpoint, replacing the API-endpoint value with the API endpoint for your region.

```$ cf api <API-endpoint>```

   | **Region name** | **Geographic location** | **API endpoint** |
   |-----------------|-------------------------|-------------------|
   | US South region | Dallas, US | api.ng.bluemix.net |
   | US East region | Washington, DC, US | api.us-east.bluemix.net |
   | United Kingdom region | London, England | api.eu-gb.bluemix.net |
   | Sydney region | Sydney, Australia | api.au-syd.bluemix.net |
   | Germany region | Frankfurt, Germany | api.eu-de.bluemix.net |
   
 login in to your IBM account
 
 ```
 $ cf login
 ```
if you cannot log in using the ```cf login``` or ```bx login``` commands because you have a federated user ID, use either the ```cf login --sso``` or ```bx login --sso``` commands to log in with your single sign on ID.

then from your cloned directory root push the app to IBM cloud.
```
$ cf push 
```

Deploying the app may take a few minutes. when done you'll see a green dot next the app name. View your app at the URL listed in the output of the push command, or view both the app deployment status and the URL by running the following command:

```
$ cf apps
``` 
 ## Step 5 : add a database.
 Add a NoSQL database to this application and set up the application so that it can run locally and on IBM Cloud.
   
  * log in to IBM Cloud and go to the Dashboard. Select your application by clicking on its name.
  * Click Connections then Create connection.
  * In the Data & Analytics section, select Cloudant NoSQL DB and then create the service.
  * Select Restage when prompted.
  * IBM Cloud will restart your application and provide the database credentials to your application.
  
 ## Step 6 : Add a tool chain to the application (CI)
A toolchain is a set of tool integrations that support development, deployment, and operations tasks. 
The collective power of a toolchain is greater than the sum of its individual tool integrations.

  * On the app overview on the Continuous delivery card, click Enable. 
  * On the "Create a Toolchain" page, review the diagram of the toolchain that you are about to create. The diagram shows each tool integration in its lifecycle phase in the toolchain. The toolchain's name identifies it in IBM Cloud. If you want to use a different name, change the toolchain's name.



 

 
