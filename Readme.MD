# Okta AWS-CLI


We have built a simple Java application that generates temporary AWS credentials using AWS STS Assume roles, this enables AWS customers to seamlessly gain access to AWS resources using Okta to as a Single-Sign-On source.

###Setup###

Use ```git clone https://github.com/rlondner/okta-aws-cli.git``` to clone the repository locally

###Configuring the application###
  It is essential that ```oktaAWSCLI.config``` be in the same directory as the ```oktaAWSCLI.jar``` file. The oktaAWSCLi config file holds information specific to each org and needs to be configured on an org to org basis. 

  Your Okta Org and AWS application url need to be added to your configuration file.
  - ```OKTA_ORG``` which is the url of your Okta org.
  - ```OKTA_AWS_APP_URL``` is the url link of your Okta AWS application url
  - **Obtaining an AWS app url**
    - Navigate to the ```Admin Dashboard``` of you Okta org 
    - Select the ```Application``` tab and click you AWS Application 
    - Under the ```General``` menu, scroll down to find the ```App Imbed Link``` section 
    - Your link is located under ```Embed Link``` 
  - Replace the example values in ```oktaAWSCLI.config``` with your values

###Running the application###
  - To run the application use the following command while in the directory containing the ```.jar``` file
  - ```java -jar oktaAWSCLI.jar```
  
