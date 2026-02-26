# Postman API Automation Integration with GitHub Actions #

This repository is demonstration for POC for Integrating Postman tests with GitHub Actions.The tests are written in Postman and executed on VM with the help of newman and newman-reporter-htmlextra.
GitHub Actions will trigger project execution on every push to the main branch.You can also execute the project manually using worflow_dispatch. The project runs on schedule wit the help of cron job.


The HTML report is archived and kept in archive section for team to download it.Along with that they can view the report directly from the github page: https://prudvikishore.github.io/Phoenix-Inwarranty-Collection-Flow/
The latest report is mailed to the team members using GMAIL SMTP.

## About Me ##
My Name is Prudvikishore Darsi. I have 12 years of experience in Manual testing of Mobile Apps(iOS and Android) and for the API Automation testing using Postman and RestAssured

## Test Coverage ##
1.Happy Flow Testing

2.Negative Testing and Edge Case Testing

3.Token Testing

4.Schema Validation

5.Data Driven testing using CSV

6.Secret Management with GitHub Secrets

## Tech Stack ##

1.Postman

2.NodeJs v22

3.newman

4.newman-reporter-htmlextra

5.GitHub Actions

6.GitHub Pages

7.AWS EC2 for Self Hosted Runner

8.GMAIL SMTP

9.CSV for data driven testing

## GitHub Pages ##
You can directly view the latest report of Postman test execution from https://prudvikishore.github.io/Phoenix-Inwarranty-Collection-Flow/


## HTML Report ##
The Report will be created in newman folder
![Postman Report](https://github.com/prudvikishore/Phoenix-Inwarranty-Collection-Flow/blob/static-content/newman-report.png)

## Project Structure ##

Phoenix Inwarranty Collection Flow
```
├─ InWarranty-Flow Collection.postman_collection.json

├─ QA.postman_environment.json

└─ testData.csv
```

## How to run the Project? ##
You can run the project on local system for that:

1.Clone the Project on local system: https://github.com/prudvikishore/Phoenix-Inwarranty-Collection-Flow.git

2.Install NodeJs and NPM from https://nodejs.org/en

3.Install newman using npm install -g newman

4.Install newman-reporter-htmlextra using npm install -g newman-reporter-htmlextra

5.Run the newman command:

              newman run 'InWarranty-Flow Collection.postman_collection.json' \
              
             -e QA.postman_environment.json \
             
             -d testData.csv \
             
             -r cli,htmlextra \
             
             --reporter-htmlextra-export ./newman/index.html
