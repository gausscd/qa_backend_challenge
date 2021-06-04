README 
v1.0 - 03/6/2021

This is a backend (API) automation testing project using Postman and Newmanl for the Square Payments API (https://developer.squareup.com/reference/square/payments-api).  

- This Repository can be found here: https://github.com/gausscd/qa_backend_challenge

- Setup:
 1. Install Node.js + npm https://nodejs.org/en/
    [You can follow this guide: https://wsvincent.com/install-node-js-npm-windows/]
 2. Recommended to use Visual Studio Code: https://code.visualstudio.com/ 
 3. From the main directory (qa_backend_challenge/) run the following commands:
	npm install -g newman
	npm install -g newman-reporter-htmlextra
	
- The repository is structured as follows:
	1. Collection file: \qa_backend_challenge\API\collection\Square Payments.postman_collection.json
	2. Environment variables: qa_backend_challenge\API\envVariables\Square Payments PROD.postman_environment.json
	3. Set of e2e tests (3), to be ran using newman: \qa_backend_challenge\e2e\Square Payments Scenarios.postman_collection.json
	4. A folder containing the reports from the execution of the scenarios: \qa_backend_challenge\API\reports\
	
- Running the tests: in order to execute the tests in the Scenario collection, run the following command from the terminal, while located at the main directory (qa_backend_challenge):
	newman run './e2e/Square Payments Scenarios.postman_collection.json' -e  './API/envVariables/Square Payments PROD.postman_environment.json' -r htmlextra --reporter-htmlextra-export './API/reports'





