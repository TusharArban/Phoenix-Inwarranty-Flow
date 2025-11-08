# Postman API Automation Intgration with Github Actions #

Thos repository is a demonstration for POC for integrating postman tests with github actions. The tests are written in Postman and they are executed on the VM with the help of newman and newman-reporter-htmlextra.
Github actions will trigger the project execution on every push to the main branch. You can also execute the project manually usin workflow_dispatch. The Projects runs on a scheduled time with the help of the cron job.

The HTML report is archived and kept in the artifact section for the team to dwonload it. Along with that they can view the report directly from the github page : https://github.com/TusharArban/Phoenix-Inwarranty-Flow

## About us ##
Hi, My name is Tushar Arban. I have 4 years of experience in Automation Testing. My Skillset includes UI Automation with Selenium Webdriver, Cypress and for API Testing I use Rest Assured and Postman.
You can connect with me over: www.linkedin.com/in/tushar-arban

## Testing Coverage ##
1. Happy flow testing
2. Negative Testing and Edge case Testing
3. Token testing
4. Data Driven testin with CSV
5. Schema validation
6. Secrets management with Github secrets

## Tech Stack ##
1. Postman
2. Node js 22v
3. Newman
4. Newman-reporter-htmlextra
5. Github Actions
6. Gmail SMTP
7. Github pages
8. CSV for Data Driven Testing
9. AWS-EC2 instance for Self hosted github runner.

## Github Pages ##
You can directly view the latest report of the Postman Test at the Github Page Link: https://tushararban.github.io/Phoenix-Inwarranty-Flow/

## HTML Report ##
The report will be created in the newman folder
![Postman Report](https://github.com/TusharArban/Phoenix-Inwarranty-Flow/blob/static-content/Screenshot%20report.jpg)

## Project Structure ##
```
Pheonix Inwarranty Flow
├─ Inwarrenty-flow Collection Data Variable.postman_collection.json   #Collection file
├─ QA.postman_environment.json   # env file
├─ README.md
└─ testData.csv   #test data file

```
## How to run the Projects? ##
You can run theproject on your local system for that:
1. Clone the Project on Local System: https://github.com/TusharArban/Phoenix-Inwarranty-Flow.git
2. Install Node js and NPM from https://nodejs.org/en/download
3. Install Newman using ``` npm install -g newman ```
4. Install Newman-reporter-reporter using ``` npm install -g newman-reporter-htmlextra ```
5. Run the newman command:
   ```
   newman run 'Inwarrenty-flow Collection Data Variable.postman_collection.json' \
          -e QA.postman_environment.json \
          -d testData.csv \
          -r cli,htmlextra \
          --reporter-htmlextra-export ./newman/index.html
```
