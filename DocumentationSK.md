# Deployment 2
## System Design
![Deployment2 drawio](https://github.com/Sameen-k/Deployment2/assets/128739962/17c98d2b-a2c8-4286-bd9e-77633470a59a)

## Steps
1. Download application files from Kura's GitHub Repo
   
2. Create your own GitHub Repo and include the Kura application files previously downnloaded (Make sure the files look the same, meaning when copying and pasting make sure the files that are in folders remain in their respective folders)
   
3. Login to Jenkins and begin to setup new pipeline. (GitHub Token will be needed. see next step)

4. Create a personal access token from GitHub (Make sure to save that token in notes in case you need it again. This will be the only time you'll be able to see it)
   
5. Complete the pipeline setup on Jenkins (Token and Repo-link needed)
    
6. Run the pipeline on jenkins and if successful, access the Jenkins Console output for documentation. Jenkins will zip the application files including the test results file. You can download the zip file from jenkins to include the test files or redownload just the application files from your GitHub Repository
Console Input Indicating zip files:
![Screen Shot 2023-08-25 at 11 40 21 PM](https://github.com/Sameen-k/Deployment2/assets/128739962/ae802974-cd5b-4f09-8e78-d26781837819)

7. Use Scribe resources to setup elastic beanstalk roles and rezip application files to use them to setup environment (To submit application files in AWS you must make sure you redownload the application files from your own repo on GitHub, unzip them all, then rezip them (make sure you  are not including the parent folder)) If you downloaded the zip file from jenkins, be sure to rezip that as well

## Launched Application 
![Screen Shot 2023-08-25 at 11 37 53 PM](https://github.com/Sameen-k/Deployment2/assets/128739962/b82dbd64-a4d7-4b1f-985e-f0771ac57c49)
## Completed Application 
![Screen Shot 2023-08-25 at 11 38 02 PM](https://github.com/Sameen-k/Deployment2/assets/128739962/d2a9139a-c9ee-4ea4-91e8-23e6abc786d9)


