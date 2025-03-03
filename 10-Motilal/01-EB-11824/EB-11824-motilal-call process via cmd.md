## 📌 Task Overview
- **Task Title:** Post Call Procees via Command
- **Task Type:** Feature
- **Assigned To:** Anas Hussain

---

## 📋 Task Description
_Post Call Procees via Command._

---

## 🛠 Steps to Complete
- [x] Make the project runnable on local
	- [x] Import mysql
	- [x] Import mongodb
- [x] Run the project on local
- [x] Create a plan for change the post-call process via command
- [x] Cross check the existing api is ready for getting the cdr data
- [x] Cross check the source code version and make a feature branch.
- [x] Create a function to store CDR data during the Airtel callback.
	- [x] create _Service_ directory
	- [x] create _cdrFileWrite_ file on service directory		
	- [x] write logic to the _cdrFileWrite_ file
- [x] Save the CDR data into a temporary file.
- [x] Create a console command to process the CDR file.
	- [ ] Write logic to CDR data processing
- [x] Activate the agent mobile app.
	- [x] Update composer.json file
	- [x] `composer update`
	- [x] `php artisan vendor:publish --tag=agentapp-config`
	- [x] Sub domain activation `php artisan subdomain:enable`
- [x] Process the CDR file and push the data to Firebase.
	- [x] Build CSV file
	- [x] Upload CSV file
	- [x] Command call
- [ ] Modify _config/agentapp.php_ file
	- [ ] 

---

## 📂 Files & Resources
- 📄 Related Documents: [Link/File Path]  
- 🔗 Reference Links: [Ticket](https://waybeo.atlassian.net/browse/EB-11824), [Link 2](#)  

---

## 🚀 Release Process
_Details on how to deploy this task to production._

### 🔹 Server Deployment
- [ ] Update .env file
	- [ ] POST_CALL_COMMAND_ARGUMENT_NAME=test
	- [ ] MOBILE_API_URL=
	- [ ] MOBILE_API_ACCESS_TOKEN=
- [ ] give file permissions to the storage directory
- [ ] create directory 
- [ ] `composer update`
- [ ] enable subdomain `php artisan subdomain:enable`

### 🔹 Database Changes
- [ ] Add a VN to a test store.
- [ ] Add agent number to the store
- [ ] update VN callflow
- [ ] add `mobile_app` column on **numbers** table set (default is 0) comment(0: disable, 1: enable)
- [ ] set `mobile_app` = 1 for agent-activated mobile numbers (csv file numbers)

---

## 🧪 Test Cases
_Instructions for testing the task before release._

### 👨‍💻 Developer Side
- [ ] Make a call - check cdr data is write / not
- [ ] Rest of the all functionalities are working
	- [ ] SI push
	- [ ] Alert SMS sent / not
- [ ] 

### 🧑‍🔬 Tester Side
- [ ] 

---

## 🐞 Issues & Challenges
- **Known Issues:**  
- **Blockers:**  

---

## 🛠 Enhancement to the Code
_Document possible improvements or future refactoring for this feature._

---

## ✅ Completion Notes
_After completing the task, summarize the final implementation details and any important learnings._

---

## 📢 Additional Comments
_Add any extra notes or feedback about the task._

---

✍️ **Last Updated:** `DDth MM YYYY`
