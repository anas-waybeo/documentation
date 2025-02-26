## 📌 Task Overview
- **Task Title:** Call report internal mail
- **Task Type:** Feature
- **Assigned To:** Anas Hussain

---

## 📋 Task Description
_Create an Internal Call Summary Report for mail sending. The report should contain call-status, call-count, call-percentage._

---

## 🛠 Steps to Complete
1. [x] Project runnable on docker
2. [x] install _dom php_ extension
3. [x] create mail via terminal `php artisan make:mail DailyCallCountReportMail`
4. [x] Create a blade file for email template
5. [x] Create a console command with `php artisan make:command SendDailyCallCountReport`
6. [x] Schedule the task on _app/console/Kernel.php_ file
	- [x] `$schedule->command('report:daily')->dailyAt('00:15');`
7. [x] Implement SRP in console command file
	- [x] Create a service file on _app/services_ directory
	- [x] Move all business logics to the _service_ file
8. [x] Run schedule via this `php artisan schedule:run`
9. [x] Update config files
	- [x] set **ses** as the default mail driver on _config/mail.php_
	- [x] set _default mail address_ 

---

## 📂 Files & Resources
- 📄 Related Documents: [Link/File Path]  
- 🔗 Reference Links: [Ticket](https://waybeo.atlassian.net/browse/EB-11702), [Link 2](#) 

---

## 🚀 Release Process
_Details on how to deploy this task to production._

### 🔹 Server Deployment
1. [x] Move files to the server
2. [x] Update **aws-mail** configurations on _.env_ file

### 🔹 Database Changes
_Nothing._

---

## 🧪 Test Cases
_Instructions for testing the task before release._

### 👨‍💻 Developer Side
- [x] Trigger the console command.
- [x] Make sure the schedule is working good.

### 🧑‍🔬 Tester Side
- [x] Make sure the email is successfully sent to the recipients.

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

✍️ **Last Updated:** `2025-02-25`
