## 📌 Task Overview
- **Task Title:** Mobile App Integration for Vodafone Idea 
- **Task Type:** Feature
- **Assigned To:** Anas Hussain

---

## 📋 Task Description
_Please activate Mobile App for Primary, Secondary and Tertiary agents of PHJ, HAR and MUM Circle stores. Store details are attached for your reference._

---

## 🛠 Steps to Complete
1. [x] Make the project runnable on docker
2. [x] Import _sql_
3. [x] Setup Mongo datalayer connection _(optional for local)_
4. [x] Create new _mobile-app_ branch on git to make the changes
5. [x] Go-through mobile app integration documentation
	1. [x] Update _composer.json_ file
	2. [x] `composer update`
	3. [x] `php artisan vendor:publish`
6. [x] Refer [WaybeoVECV](https://github.com/WaybeoEB/WaybeoVECV) repository for refference
	1. [x] Push Call Log in the time of CDR processing. All the code setup are written in a utility file. Then call the log push to the firebase method on the CDR processing.
7. [x] Integration logic implementation
	1. [x] Create a file on _app/customLibraries/Utils/CommonUtils.php_ (copy), usages are added below
		1. Send telegram alert
		2. Fetch old call logs from mongoclient
		3. Push the processed data to the firebase
	2. [x] Add firebase-data-push logic to the post-call-utility class.
8. [x] Update the _config/agentapp.php_ file
	1. [x] make sure the calllog array data is same as the eb-call-log data
	2. [x] make sure the _CallStatuses_ based on the eb-dashboard data (Now we only process the statuses are Answered and Missed. Because EB only map the above statused call logs.)
9. [x] Prepare the csv file for agent mobile app bulk activation.
10. [x] Test the process with [webhook-site](https://webhook.site/)
11. [x] Git push
	1. [x] create a new branch _release-1.3.0_ from _mobile-app_ branch
	2. [x] release that on UAT
	3. [x] merge _development_ branch and _main_ branch with  _release-1.3.0_.



---

## 📂 Files & Resources
- 📄 Related Documents: [Link/File Path]  
- 🔗 Reference Links: [Ticket](https://waybeo.atlassian.net/browse/EB-11642), [Link 2](#)  

---

## 🚀 Release Process
_Details on how to deploy this task to production._

### 🔹 Server Deployment
1. Push the source code to mobile-app git branch.
2. Release the changes on UAT server.
3. Update below details in .env file
	1. APP_NAME=VodafoneTest
    2. MOBILE_API_URL=
    3. MOBILE_API_ACCESS_TOKEN=
4. Enable sub-domain by below steps
	1. cd projectFolderPath/
	2. `composer update`
	3. `php artisan mobile-subdomain:enable`
5. Postman API – call for csv file upload.
6. Restart post-call process	

### 🔹 Database Changes
1. Add a VN to a test store.
2. Add agent number to the store
3. update VN callflow
4. add `mobile_app` column on **numbers** table set (default is 0) comment(0: disable, 1: enable)
5. set `mobile_app` = 1 for agent-activated mobile numbers (csv file numbers)

---

## 🧪 Test Cases
_Instructions for testing the task before release._

### 👨‍💻 Developer Side
- [x] check the agent-mobile status php `artisan mobile-agent:check --agent=8078499987`
- [x] enable agent-mobile `php artisan mobile-agent:enable --code=ABC –agent=8078499987`
- [x] disable agent-mobile `php artisan mobile-agent:disable --agent=8078499987`
- [x] Test the process with [webhook-site](https://webhook.site/)
- [x] Test file csv file uploading via postman.

### 🧑‍🔬 Tester Side
- [x] Download the mobile application _waybeo agent app_
- [x] Login with agent mobile number
- [x] Process CRD data
- [x] Make sure the data is refelected on mobile app
- [x] Make sure the all numbers are found on the users dump file

---

## 🐞 Issues & Challenges
1. In the time of csv file preperation all the values are case-sensitive otherwise it won’t work.
2. Csv file maximum no of rows is 50. If agents mobile number is above 50, split the csv file.

---

## 🛠 Enhancement to the Code
1. Make the agent app utility repository to package. Upload the package to packagist
2. Implement SOLID principles
3. Write php-unit test cases for reliability

---

## ✅ Completion Notes
_After completing the task, summarize the final implementation details and any important learnings._

---

## 📢 Additional Comments
1. An agent no is only for a subdomain
2. How to enable more agents
	1. make the csv file.
	2. set mobile_app = 1 on the numbers table
3. The data should be displayed from the time of mobile activation. Old data process is not handled.

---

✍️ **Last Updated:** `14th Feb 2025`
