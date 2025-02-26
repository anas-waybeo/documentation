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
4. [ ] Find the reason of why _StoreManager_ value is **null**
	- [x] Process the cdr and how data is formatting
	- [ ] Call-log data building time _StoreManager_ name is taking from **stores** table
		- [x] Make sure _store_manager_name_ is update on the time of update **stores** details
		- [ ] Some times the _store_manager_name_ is empty in the **stores** table. check that
		- [ ] rewrite the logic, take _store_manager_name_ only from **store_managers** table
5. [ ] Change the data fetching logic through out the app
	- [ ] Delete _store_manager_name_ column from **stores** table
	- [ ] Fix the above change to the _post_call_operation_

---

## 📂 Files & Resources
- 📄 Related Documents: [Link/File Path]  
- 🔗 Reference Links: [Ticket](https://waybeo.atlassian.net/browse/EB-11683), [Link 2](#) 

---

## 🚀 Release Process
_Details on how to deploy this task to production._

### 🔹 Server Deployment
_Step-by-step instructions for deploying changes to the server._  

### 🔹 Database Changes
_Script details, migration steps, or schema updates required._

---

## 🧪 Test Cases
_Instructions for testing the task before release._

### 👨‍💻 Developer Side
- [ ] Unit tests  
- [ ] API tests  
- [ ] Integration tests  

### 🧑‍🔬 Tester Side
- [ ] Functional testing  
- [ ] Regression testing  
- [ ] Performance testing  

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

✍️ **Last Updated:** `YYYY-MM-DD`
