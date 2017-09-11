# QA testing process for Android Apps:
## We do both 
1.	Automation Testing
1.	Manual Testing.

## 1. Automation Testing

#### Technology and Tools Used in Automation
1)	Java (Core Java as well as Advanced Java)
2)	Selenium
3)	Selenium Grid
4)	Appium
5)	TestNG
6)	Maven (Dependency Management)
7)	Uiautomatorviewer (Element Inspector)

#### Framework and Its Features:
1)	Data Driven Framework
2)	Apache POI API (for excel interaction)
3)	Advanced reporting 
4)	Logging (Adb logs, App specific logs & Automation logs)
5)	Result backup
6)	Screenshots
7)	Automatic mail triggering to specific people on completion of test

#### Reporting and Its Features:
1)	Extent Report API
2)	Captures Pass, Fail & Not Run test cases
3)	Captures Start & End time of automation tests
4)	Graphical representation of test result & status
5)	Capture fail test screenshot
6)	Logs
7)	Time taken to complete a test
8)	Company logo

#### Model:
1)	Page Object Model 

#### Types of Testing doing through Automation:
1)	Smoke Test
2)	Basic Functionality Test
3)	Monkey Test (Based on numbers of random event on android package)


## 2. Manual Testing 
> Following is the process we follow for manual testing
1. 	Understand the functionality of the feature
1.	Create Test plan/test scenarios/test cases for the feature.
1.	Get it peer reviewed.
1.	Prepare the test data (test users, test configuration, test clients etc.)
1.	Complete the test execution for all the cases.

## Release Checklist:
1.	Make sure that there are no high critical/blocker issues (no bugs with status “Major/Blocker/Critical”.
1.	For low priority, important issues, take a call from product owner whether it is good to go with those issues.
1.	Sanity and Regression testing on the final build
1.	Make sure the release notes are proper.
