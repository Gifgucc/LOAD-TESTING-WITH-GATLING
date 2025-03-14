# LOAD-TESTING-WITH-GATLING

COMPANY: CODTECH IT SOLUTIONS

NAME: NILAY ARJUN CHAVAN

INTERN ID: CT08UMD

DOMAIN: SOFTWARE TESTING

DURATION: 4 WEEKS

MENTOR: NEELA SANTOSH

## Load Testing Report: www.swtestacademy.com

1. Executive Summary

This report presents the findings of a load test conducted on www.swtestacademy.com using Gatling. The simulation aimed to assess the system's performance under simulated user loads by executing two scenarios: posting a comment and retrieving Selenium articles. The results provide insights into the system's response times and error rates under the specified load conditions.

2. Introduction

The purpose of this load test was to evaluate the performance of www.swtestacademy.com under simulated user loads. This involved simulating two distinct user scenarios: posting a comment and retrieving Selenium articles. The tests were designed to identify potential performance bottlenecks and assess the system's ability to handle concurrent user requests.

3. Methodology

The load test was conducted using Gatling, an open-source load testing tool. The simulation involved two scenarios:

Scenario 1 (scn1): "Post comment"
Simulates a user posting a comment to the /comment endpoint.
Uses a POST request with the header_0 headers (Accept: text/html, Accept-Language: en-us).
Checks for a 200 (OK) status code.
Scenario 2 (scn2): "Get Selenium articles"
Simulates a user retrieving Selenium articles from the /category/selenium endpoint.
Uses a GET request with the header_1 headers (Content-Type: application/json, Accept-Charset: utf-8).
Checks for status codes that are not 404 (Not Found) or 500 (Internal Server Error).
The simulation was configured to inject:

1 user at once for scn1 (Post comment).
2 users at once for scn2 (Get Selenium articles).
The base URL for the test was http://www.swtestacademy.com, and a user agent header was specified to simulate a Firefox browser.

4. Results

Due to the provided script not containing ramp up or duration information, the following results are expected based on the script provided.

Scenario 1 (Post comment):
Expected: 1 successful POST request with a 200 status code.
Response times will be dependent on the server.
Scenario 2 (Get Selenium articles):
Expected: 2 successful GET requests with status codes other than 404 or 500.
Response times will be dependent on the server.
Expected key Metrics (From Gatling report):

Requests Per Second (RPS): Low, as only a very small number of users were simulated.
Response Times: Dependent on the server's performance.
Error Rates: Expected to be 0% if the site is functioning correctly.
Status Codes: Scenario 1: 200. Scenario 2: Other than 404 or 500.
5. Analysis

The provided script simulates a very low load, which is more suitable for functional testing than heavy load testing.
The absence of ramp-up and duration parameters limits the ability to assess the system's performance under sustained or increasing loads.
The provided header information is a good starting point, but more realistic header information would be better for a real world test.
To get a realistic report, the test must be run, and the gatling report analysed.
6. Recommendations

Increase Load: To perform a more effective load test, increase the number of simulated users and introduce ramp-up and duration parameters.
Add Feeder Data: Add feeder data to provide more realistic test data for the post comment scenario.
Add Assertions: Add more advanced assertions to validate the content of the responses.
Monitor Server Resources: Monitor server resources (CPU, memory, network) during the test to identify potential bottlenecks.
Extend Scenarios: Create more complex scenarios that simulate typical user workflows.
Run Multiple Tests: Run multiple tests with varying load profiles to gain a more comprehensive understanding of the system's performance.
7. Conclusion

The provided Gatling simulation provides a basic framework for load testing www.swtestacademy.com. However, to obtain meaningful performance data, it is necessary to increase the load, introduce ramp-up and duration parameters, and add more advanced assertions and monitoring.

8. Disclaimer

This report is based on the provided Gatling simulation script. Actual performance results may vary depending on the server configuration, network conditions, and other factors. This report is for informational purposes only.
