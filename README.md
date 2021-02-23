# JMeter-Tests

JMeter advantages

Easy to use without extensive knowledge of programming. ...
Provides integration with Jenkins and reporting.
Easy installation on any operating system.
Key features like the Thread Group, helps to see whether software performance is good.
Test IDE allows test recording from browsers or native applications

Creates a request and sends the request to the server
Collects responses from the server and visualizes the details in a chart or graph
Processes the response from the server
Generates test results in several formats such as text, XML, JSON for the tester to analyze data
Test IDE allows test recording from browsers or native applications
Allows API testing, Database Testing, and MQ testing with ease
When there’s a high number of TPS, one can achieve more transactions per second given the hyper-limitations.

Disadvantages of JMeter

Automation is difficult with JMeter
JMeter output reports are difficult to understand without training
It doesn’t support JavaScript and AJAX requests.
Complex applications that use dynamic content or use JS to alter requests can be difficult to test using JMeter.
It’s difficult to get data from one place or to perform customizations.

JMetre Notes to prepare different type of test cycles

Create Basic Test Case

1. Test Plan
2. Add thread groups (Users)
3. Add Samplers (Http Requests)
4. Add Listners (Results)
5. You can also add Assertion by giving expected result(Optional)
6. Save and Run and validate


Record UI and run in JMeter

1. Add Blazemeter chrome extension
2. Open any website and record the site using blaze meter
3. Save the record script and export in Jmeter-JMX
4. Open recorded script in JMeter
5. Run and validate

CSV Config Test in JMeter using JAVA Reques

1. Create Data.csv file (Give some data in it ex: Firstname and Lastname and add some names and save)
2. Open JMeter and ad Config Element> CSV Data set config
3. Upload/import Data.csv file using Browse button
4. Add thread group>Java Request
5. Add variables (ex: Request${Firstname} ${Lastname}
6. Add Listner (Result)
7. Save, Run and validate

Similarly you add HTTP Headers also

1. Record website (ex: Login details) using Blazemeter
2. Import recorded script in JMeter
3. Add listener (Result)
4. Save and Run and Validate
5. You can see HTTP Header/cookie/cache Managers above where if you have any API headers you can add there by using ADD/DELETE buttons below


Connect with DataBase

1. Add thread>Config>JDBC Connect configuration
2. Use your own database and take URL, Class(Mysql jar if you are using mysql), username password etc…
3. And also give variable name here (above)(ex: test)
4. Add JDBC Request - Add from Thread>Add>Sampler>JDBC Requset - 
5. And also give variable name here (above)(ex:test)
6. Select query type and Here you need to put your actual query (Get tables /data from your own DB ex: Select * from Name table)
7. Add Listners (Results in Tree/Table)
8. Save, Run and Validate

REST API Tests with JMeter (GET, POST, PUT (Update), DELETE….)

GET

1. Create Test Plan
2. Add thread group
3. Add Sampler>HTTP Request
4. Add Servernae, Path, Parameter (If needed) (ex: https://reqres.in/api/users?page=2  here rears is server name, /api/users is path name and page=2 is parameter (add parameter and give values))
5. You can also add HTTP Header Manager (For content XML, Json..etc) or HTTP Authorization if you want to give username and password..etc (IF NEEDE ONLY)
6. Add Listners (Result Tree/Table)
7. Save, Run and validate

POST 
1. Use same above methods except
2. GET method select POST method
3. Add Body and  (Take it from https://reqres.in/ )
4. Don’t add parameters
5. Add authorisation or content type if you want using HTTP manager/auth…
6. Save, Run and validate



