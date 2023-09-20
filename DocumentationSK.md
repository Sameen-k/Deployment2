# Deployment 2

## Purpose 
The purpose of this deployment was to build and test the URL Shortener application on a personally hosted Jenkins server. The URL shortener application can be used to shorten unnecessarily long URLs into a small and more concise one.

## System Design
![Deployment2 drawio](https://github.com/Sameen-k/Deployment2/assets/128739962/17c98d2b-a2c8-4286-bd9e-77633470a59a)

## Steps
1. Download application files from Kura's GitHub Repo
   
2. Create your own GitHub Repo and include the Kura application files previously downloaded (Make sure the files look the same, meaning when copying and pasting make sure the files that are in folders remain in their respective folders)

3. Install Jenkins, make sure to add the additional Jenkins plugin called "Pipeline Utility Steps"
   
4. Login to Jenkins and begin to set up a new pipeline. (GitHub Token will be needed. see next step)

5. Create a personal access token from GitHub (Make sure to save that token in notes in case you need it again. This will be the only time you'll be able to see it)
   
6. Complete the pipeline setup on Jenkins (Token and Repo-link needed)
    
7. Run the pipeline on Jenkins and if successful, access the Jenkins Console output for documentation. Jenkins will zip the application files including the test results file. You can download the zip file from Jenkins to include the test files or redownload just the application files from your GitHub Repository
Console Input Indicating zip files:
![Screen Shot 2023-08-25 at 11 40 21 PM](https://github.com/Sameen-k/Deployment2/assets/128739962/ae802974-cd5b-4f09-8e78-d26781837819)

### The image above shows Jenkin's console output where it indicates the location of the zip file it creates. To unzip these files you can head back to the terminal following this path and install unzip on the ec2 to unzip the files into a new folder 

9. Use Scribe resources to set up elastic beanstalk roles and rezip application files to use them to set up the environment (To submit application files in AWS you must make sure you re-download the application files from your own repo on GitHub, unzip them all, then rezip them (make sure you  do not include the parent folder)) If you downloaded the zip file from Jenkins, be sure to rezip that as well

### Launched Application 
![Screen Shot 2023-08-25 at 11 37 53 PM](https://github.com/Sameen-k/Deployment2/assets/128739962/b82dbd64-a4d7-4b1f-985e-f0771ac57c49)
### Completed Application 
![Screen Shot 2023-08-25 at 11 38 02 PM](https://github.com/Sameen-k/Deployment2/assets/128739962/d2a9139a-c9ee-4ea4-91e8-23e6abc786d9)

## Issues
There were issues with extracting the zip file after Jenkins rezipped it due to permission issues. 
In order to unzip the zip file you must grant the file read and write permissions using this command:

``sudo chmod u+rwx 1.0.0.1.zip`` 

Then you can unzip the file into a folder using the following command:

``sudo unzip 1.0.0.1.zip -d jenkinsD2``

## Optimization
There are many ways to improve the deployment such as automating the environment launch and the Jenkins server setup.

