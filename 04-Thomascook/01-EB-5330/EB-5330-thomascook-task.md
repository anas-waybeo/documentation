## 📌 Task Overview
- **Task Title:** Select _Region_ and _Store Manager_ filter is not working
- **Task Type:** Bug fix
- **Assigned To:** Anas Hussain

---

## 📋 Task Description
_"Select Region" and “Select Store Manager” filter is not working and showing no data._

---

## 🛠 Steps to Complete
1. [x] Typecast storemanagerid to ineger before data save to mongodb _CDR push_
2. [x] Typecast existing data’s on mongodb
3. [ ] Mongoquery to typecaste string into integer without date
```
db.calllogs.find({ StoreManagerId: { $type: 2 } }).forEach(function(doc) {
    db.calllogs.update(
        { _id: doc._id },
        { $set: { StoreManagerId: parseInt(doc.StoreManagerId) } }
    );
});
```
4. [ ] Mongoquery to typecaste string into integer with date
```
db.calllogs.find({ 
    StoreManagerId: { $type: 2 }, 
    Date: { $gte: "2025-01-01", $lte: "2025-01-31" } 
}).forEach(function(doc) {
    db.calllogs.update(
        { _id: doc._id },
        { $set: { StoreManagerId: parseInt(doc.StoreManagerId) } }
    );
});
```
4. [ ] Mongoquery to select all integer type documents `db.calllogs.find({ StoreManagerId: { $type: 16 } });`
5. [ ] Mongoquery to select all string type documents `db.calllogs.find({ StoreManagerId: { $type: 2 } });`

---

## 📂 Files & Resources
- 📄 Related Documents: [Link/File Path]  
- 🔗 Reference Links: [Ticket](https://waybeo.atlassian.net/browse/EB-5330), [Link 2](#)  

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
- [x] Nothing  

### 🧑‍🔬 Tester Side
- [ ] Make a call and do the filter
- [ ] Do the filter with existing data
- [ ] Make sure the filter is wokring good. 

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
1. Mongoquery for typecast from integer to string
```
db.st.find({ age: { $type: "number" } }).forEach(function(doc) {
    db.st.updateOne(
        { _id: doc._id },
        { $set: { age: doc.age.toString() } }
    );
});
```
2. Mongoquery for typecast from string to integer
```
db.st.find({ age: { $type: "string" } }).forEach(function(doc) {
    db.st.updateOne(
        { _id: doc._id },
        { $set: { age: parseInt(doc.age) } }
    );
});
```

---

✍️ **Last Updated:** `27th Feb 2025`
