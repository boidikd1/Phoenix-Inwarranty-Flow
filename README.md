# Postman API Automation Integration with Github Actions

This repository is demonstration for POC for integrating postman tests with github actions. The tests are written in postman and they are executed on the virtual machine with the help of newman and newman-reporter-htmlextra. 
Github Actions will trigger the project execution on every push to the main branch. You can also execute the project manually using workflow_dispatch. The projects run on scheduled time with the help of the cron job.

The HTML report is archieved and kept in the artifact section for the team to download. Along with that they can view the report directly from github page: https://boidikd1.github.io/Phoenix-Inwarranty-Flow/
The latest report is mailed to the team members using GMAIL SMTP.

## About Me ##
My name is Boidik Das. I have 3.6 years of experience in Automation,manual and API testing.

## Testing Coverage ##
1. Happy flow testing
2. Negative testing and Edge case testing
3. Token Testing
4. Data Driven testing with CSV
5. Schema Validation
6. Secrets management with Github Secrets
7. 
## Tech Stack ##
1. Postman
2. Nodejs 22v
3. Newman
4. Newman-Reporter-Htmlextra
5. Github Actions
6. 6.Gmail SMTP
7. Github Pages
8. CSV for data driven testing
9. AWS EC2 instance for self hosted github runner

## Github Pages ##
You can directly view the latest test report of the Postman test at the Github page Link: https://boidikd1.github.io/Phoenix-Inwarranty-Flow/

## HTML Report ##
The report will be ctreated on newman folder
![Postman Report](https://github.com/boidikd1/Phoenix-Inwarranty-Flow/blob/static-content/newman-report.png)

## Project Structure ##

```
Phoenix_Inwarranty_Flow
├─ In-Warranty-flow Collection Final using csvdata.postman_collection.json #Collection file
├─ QA.postman_environment.json #Environment file
└─ testdata.csv #testdata file

```

## How to run the Project? ##
You can run the project on your local system for that:
1. Clone the project on local system: https://boidikd1.github.io/Phoenix-Inwarranty-Flow/
2. Install NodeJS and NPM from https://nodejs.org/en
3. Install Newman using ``` npm install -g newman ```
4. Install newman-reporter-htmlextra:
   ``` npm install -g newman-reporter-htmlextra ```
5. Run the Newman Command:
      ```
      newman run 'Inwarranty-flow Collection.postman_collection.json' \
      -e QA.postman_environment.json \
      -d testdata.csv \
      -r cli,htmlextra \
      --reporter-htmlextra-export ./newman/index.html
      ```



   
