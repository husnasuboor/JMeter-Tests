
# Used tools to create JMeter test cases
1. JMeter tool
2. Blazemeter chrome extension for UI recorded scripts in JMeter-JMX file format
3. Data.CSV file (Dummy)

# Steps to run JMeter-tests:
Import the tests on to JMeter and execute the tests 
Able to increase Number of threads(users), Rampup time period and Loop count (According to your need)

# Steps to run CSV config test
1. Import CSVDataConfigTest.jmx file
2. Browse dowloaded Data.csv file to CSV Data Config
3. Save, Run and validate



# JMetre Notes to prepare different type of test cycles

# Create Basic Test Case

1. Test Plan
2. Add thread>thread groups(Users)
3. Increase Number of threads(users), Rampup time period and Loop count (According to your need)
4. Right click on thread group and add Samplers (Http Requests)
5. Give Server name/IP, Path and select HTTP Request (ex: GET, POST..)
6. Right click on thread group and add Listners (Results) (Results can see in: Table format/Tree format/Graph format/Logs format)
7. You can also add Assertion by giving expected result(Optional)
8. Save, Run and validate the result


# Record UI and run in JMeter

1. Add Blazemeter chrome extension
2. Open any website and record the site using blaze meter
3. Save the recorded script and export in Jmeter-JMX file
4. Open/import recorded script in JMeter
5. Add Listners to view results (Results can see in: Table format/Tree format/Graph format/Logs)
6. Save, Run and validate the result

# CSV Config Test in JMeter using JAVA Request

1. Create Data.csv file on ypur Desktop/any location (Give some data in it ex: Add Firstname,Lastname columns and add some data in it then save)
2. Open JMeter right click on Test plan and add Config Element> CSV Data set config
3. Browse Data.csv file from your location using Browse button
4. Add thread group>Java Request
5. Add variables (ex: Request${Firstname} ${Lastname})
6. Add Listner (to view Result)
7. Save, Run and validate

# Connect with DataBase

1. Add Config element>JDBC Connection configuration
2. Use your own database and take URL, Class(Mysql jar if you are using mysql), username, password etc…
3. And also give variable name (ex: test)
4. Add JDBC Request - Add from Thread>Add>Sampler>JDBC Requset - 
5. And also give variable name here (ex:test)
6. Select query type and give your actual query (Get tables /data from your own DB ex: Select * from Name table)
7. Add Listners (Results in Tree/Table format)
8. Save, Run and Validate the result

# REST API Tests with JMeter (GET, POST, PUT (Update), DELETE….)

GET

1. Create Test Plan
2. Add thread group
3. Add Sampler>HTTP Request
4. Add Servernae, Path, Parameter (If needed) (ex: https://reqres.in/api/users?page=2  here reqres is server name, /api/users is path name and page=2 is parameter 
5. You can also add HTTP Header Manager (For content XML, Json..etc) or HTTP Authorization if you want to give username and password..etc (IF NEEDE ONLY)
6. Add Listners (Result Tree/Table)
7. Save, Run and validate

POST 
1. Use same above methods except
2. GET method select POST method
3. Add Body and  (Take it from https://reqres.in/ )
4. Don’t add parameters
5. Add authorisation or content type if you want, using HTTP manager/auth…
6. Save, Run and validate

You can able to add HTTP Header Manager/cookie Manager/cache Manager (If you have any API headers, you can add there by using ADD/DELETE buttons below)



# Advantages of JMeter

1.	Easy to use without extensive knowledge of programming.
2.	Provides integration with Jenkins and reporting.
3.	Easy installation on any operating system.
4.	Key features like the Thread Group, helps to see whether software performance is good.
5.	Test IDE allows test recording from browsers or native applications
6.	Creates a request and sends the request to the server
7.	Collects responses from the server and visualizes the details in a chart or graph
8.	Processes the response from the server
9.	Generates test results in several formats such as text, XML, JSON for the tester to analyze data
10.	Test IDE allows test recording from browsers or native applications
11.	Allows API testing, Database Testing, and MQ testing with ease
12.	When there’s a high number of TPS, one can achieve more transactions per second given the hyper-limitations.


# Disadvantages of JMeter

1.	Automation is difficult with JMeter
2.	JMeter output reports are difficult to understand without training
3.	It doesn’t support JavaScript and AJAX requests.
4.	Complex applications that use dynamic content or use JS to alter requests can be difficult to test using JMeter.
5.	It’s difficult to get data from one place or to perform customizations.
