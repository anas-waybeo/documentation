## 📌 Task Overview
- **Task Title:** Store manager name is not showing
- **Assigned To:** Anas Hussain

---

## 📋 Task Description
_After the store update, the manager's name is not appearing on the report page or in the exported file._

---

## 🛠 Steps to Complete
1. [x] Run the project on docker
2. [x] Make sure _StoreManager_ value is null on mongodata
3. [x] Make sure _StoreManager_ value is updated on the below tables after update the store page
	- [x] **stores** table
	- [x] **store_managers** table
4. [x] Find the reason of why _StoreManager_ value is **null**
	- [x] Process the cdr and how data is formatting
	- [x] Call-log data building time _StoreManager_ name is taking from **stores** table
		- [x] Make sure _store_manager_name_ is update on the time of update **stores** details
		- [x] Some times the _store_manager_name_ is empty in the **stores** table. check that
		- [x] rewrite the logic, take _store_manager_name_ only from **store_managers** table
5. [x] Change the data fetching logic through out the app
	- [ ] Delete _store_manager_name_ column from **stores** table
	- [x] Make sure the _store_manager_name_ should fetch from **store_managers** table on Store page
	- [x] During the _CDR processing_ take _store_manager_name_ from **store_managers** table
6. [x] Add POST_CALL_COMMAND_ARGUMENT_NAME=test on .env file
7. [x] Do the validation on postcall operation

---

## 📂 Files & Resources
- 📄 Related Documents: [Link/File Path]  
- 🔗 Reference Links: [Ticket](https://waybeo.atlassian.net/browse/EB-11683), [Link 2](#)

---

## 🚀 Release Process
_Details on how to deploy this task to production._

### 🔹 Server Deployment
- [x] Take pull on UAT
- [x] Add POST_CALL_COMMAND_ARGUMENT_NAME=test on .env file
- [x] run `php artisan config:clear`
- [x] run postcall operation `php artisan post-call-operations:samsung test`

### 🔹 Database Changes
_Script details, migration steps, or schema updates required._

---

## 🧪 Test Cases
_Instructions for testing the task before release._

### 👨‍💻 Developer Side
- Nothing 

### 🧑‍🔬 Tester Side
- [ ] Make a call and check the _report_ page  

---

## 🐞 Issues & Challenges
1. Some stores are not assigned _store managers_. that should be empty

---

## 🛠 Enhancement to the Code
_Nothing._

---

## ✅ Completion Notes
_After completing the task, summarize the final implementation details and any important learnings._

---

## 📢 Additional Comments
_Add any extra notes or feedback about the task._

---

✍️ **Last Updated:** `26th Feb 2025`
