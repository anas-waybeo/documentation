## 📌 Task Overview
- **Task Title:** HP export error
- **Task Type:** bug fixing
- **Assigned To:** Anas Hussain

---

## 📋 Task Description
_Total conversation duration(in min) is not exported._

---

## 🛠 Steps to Complete
1. [x] Make project runnable on local
2. [x] The Reason is found in the **data-maping from mongodata and revert it to the dashboard**.
	- [x] Map the data before execute the mongo-query.
	- [x] Map the data again after execute the mongo-query.
3. [x] Push the changes to _hotfix-v1.0.0_ branch

---

## 📂 Files & Resources
- 📄 Related Documents: [Link/File Path]  
- 🔗 Reference Links: [Ticket](https://waybeo.atlassian.net/browse/EB-5433), [Link 2](#)  

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
- [ ] Nothing 

### 🧑‍🔬 Tester Side
- [ ] Login as admin
- [ ] Export report data
- [ ] Make sure the exported file has _TotalConversationDuration_ value.

---

## 🐞 Issues & Challenges
- Data name change before and after database operation 

---

## 🛠 Enhancement to the Code
1. Implement _unit test_

---

## ✅ Completion Notes
_After completing the task, summarize the final implementation details and any important learnings._

---

## 📢 Additional Comments
1. Bug is fixed on the admin dashboard report page.
2. Data is not available on the ob_report page

---

✍️ **Last Updated:** `27th Feb 2025`
