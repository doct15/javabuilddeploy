SimpleJavaApp
==============

A simple java app with a distelli-spec.yml file that describes how this app should be deployed using the Distelli platform.

### Before you deploy
 - <a href="http://www.distelli.com/docs/setup.html" target="_blank">Setup the Distelli Agent</a> on the server that you want to deploy this app to
 - <a href="http://www.distelli.com/docs/setup-cli.html" target="_blank">Setup the Distelli CLI</a> on your desktop machine
 
### Prerequisites

This app requires the Java JRE which must be present on the server you're deploying to.

### Deploying

You can deploy this app with the following easy steps:

 - **Clone this repo**: <br/>
    ``git clone git://github.com/distelli/SimpleJavaApp.git``

 - **Update the distelli-spec.yml** <br/>
     In the distelli-spec.yml file, change the values for JAVA_HOME (in the RuntimeVars sections)to point to the directory where the JRE is installed on your server.

 - **Push the code to your S3 bucket using the Distelli CLI** <br/>
   ``distelli push -m "My first deployment"`` <br/>

 - **Deploy using the distelli Web interface** <br/>
   The Simple Java app should now be available in your distelli account. Click New Deployment in your account and fill in the details to start the deployment.

 - **Make a request** <br/>
   Once the deployment is done, click the SimpleJavaApp in your list of applications and you should see it running on the server you deployed to. Make a request using your browser to http://&lt;server&gt;:8080/ and you should see the app running on your server.
