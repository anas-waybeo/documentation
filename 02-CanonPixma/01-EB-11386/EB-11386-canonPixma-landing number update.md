## 📌 Task Overview
- **Task Title:** Landing number update
- **Task Type:** feature
- **Assigned To:** Anas Hussain

---

## 📋 Task Description
_Create a validation for the service number update section. Ensure it only accepts 11-digit numbers starting with 18._

---

## 🛠 Steps to Complete
1. [x] Create a new js function to check the number is valid
2. [x] Check the validation function during the form submission
3. [x] Database callflow validation
	- [x] If 10-digit number +91 prefix before use the no.
	- [x] If 11-digit number directly use the no.
4. [x] 

---

## 📂 Files & Resources
- 📄 Related Documents: [Link/File Path]  
- 🔗 Reference Links: [Ticket](https://waybeo.atlassian.net/browse/EB-11386), [Link 2](#)  

---

## 🚀 Release Process
_Details on how to deploy this task to production._

### 🔹 Server Deployment
1. [x] Push the changes to the _hotfix-v1.0.0_ branch
2. [x] merge it with _development_ and _master_
	[x] git checkout hotfix-v1.0.0
	[x] git pull origin hotfix-v1.0.0
	[x] git checkout master
	[x] git merge --no-ff hotfix-v1.0.0 -m "Merge hotfix-v1.0.0 into master" 
	[x] git push origin master
	[x] git tag -a v1.1.5 -m "11-digit landing no update"
	[x] git push origin v1.1.5
	[x] git checkout development
	[x] git merge --no-ff hotfix-v1.0.0 -m "Merge hotfix-v1.0.0 into development"
	[x] git push origin development

3. [x] Set CALLFLOW_URL=http://callflow-uat.waybeo.com in .env file
4. [x] run `php artisan config:clear`

### 🔹 Database Changes
_Nothing._

---

## 🧪 Test Cases
_Instructions for testing the task before release._

### 👨‍💻 Developer Side
- [x] Update the service number
- [x] Make sure the callflow
	- [x] 10-digit no add +91 as prefix
	- [x] 11-digit no use the no

### 🧑‍🔬 Tester Side
- [ ] Update a service no.
- [ ] Make a call and check is it working fine

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

✍️ **Last Updated:** `2025-02-26`
