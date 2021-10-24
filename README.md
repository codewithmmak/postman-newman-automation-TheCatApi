# API Automation using POSTMAN and running tests using Newman 

## How to run Postman Collection using Postman tool?
1. Open Runner
2. Drag and Drop your collection
3. Select the tests
4. Hit Run button
![API Automation using POSTMAN and running tests using Newman](./img/Test_Runner_01.png?raw=true "POSTMAN Test Runner")

## How to run Postman Collection using Newman CLI tool?
1. Open Terminal/CMD
2. Install newman `npm install -g newman`
3. Go to root path of the project
4. Enter command
`newman run TheCatAPI.postman_collection.json --environment TheCatAPI_Env.postman_environment.json`
5. CLI will show below results

![API Automation using POSTMAN and running tests using Newman Console Output 1](./Img/Console_01.png?raw=true "API Automation using POSTMAN and running tests using Newman Console Output 1")

![API Automation using POSTMAN and running tests using Newman Console Output 2](./Img/Console_02.png?raw=true "API Automation using POSTMAN and running tests using Newman Console Output 2")

## How to generate HTML report using npm newman-reporter-htmlextra with Newman?
1. Open Terminal/CMD
2. Install reporters `npm install -g newman-reporter-htmlextra`
3. Go to root path of the project
4. Enter command
`newman run TheCatAPI.postman_collection.json --environment TheCatAPI_Env.postman_environment.json -r htmlextra --reporter-htmlextra-export .\TestResults\TestResult.html`

![API Automation using POSTMAN and running tests using Newman](./Img/Newman_Report_01.png?raw=true "API Automation using POSTMAN and running tests using Newman Test Results 1")

![API Automation using POSTMAN and running tests using Newman](./Img/Newman_Report_01.png?raw=true "API Automation using POSTMAN and running tests using Newman Test Results 2")

![API Automation using POSTMAN and running tests using Newman](./Img/Newman_Report_01.png?raw=true "API Automation using POSTMAN and running tests using Newman Test Results 3")

## How to generate CSV report using npm newman-reporter-csv with Newman?
1. Open Terminal/CMD
2. Install reporters `npm install -g newman-reporter-csv`
3. Go to root path of project
4. Enter command
`newman run TheCatAPI.postman_collection.json -r csv --reporter-csv-export .\testResults\TestResult.csv`

## Troubleshooting
Issue #1: When you run Postman collection using newman you may see error: 

File C:\Users\admin\AppData\Roaming\npm\newman.ps1 cannot be loaded because running scripts is disabled on this system. For more information, see about_Execution_Policies at https:/go.microsoft.com/fwlink/?LinkID=135170.

Solution: Follow step 1 to 3 given on `https://www.c-sharpcorner.com/article/how-to-fix-ps1-can-not-be-loaded-because-running-scripts-is-disabled-on-this-sys/`
