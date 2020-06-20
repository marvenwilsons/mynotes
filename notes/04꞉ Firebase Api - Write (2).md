---
tags: [Firebase]
title: '04: Firebase Api - Write'
created: '2020-06-09T21:04:08.764Z'
modified: '2020-06-10T18:14:13.654Z'
---

## 04: Firebase Api - Write
- First we need to get the reference of the traget node
- then we use the firebase database set method to add data to that node

Sample data: Jane Doe's data, jane done is a firebase user with a user id of `AKJSDVNQIUWE`
```json
{
  "task": {
    "AKJSDVNQIUWE: {
      "task1": {},
      "task2": {},
      "task3": {}
    }
  }
}
```


```javascript
import { firebaseAuth, firebaseDb } from 'firebase.js'
 
// get user uid, jane doe's id
const userId = firebaseAuth.currentUser.uid
 
// get tasks
const userTasks = firebaseDb.ref('/task', + userId)

const updateObject = {/** ... */}
userTasks.set(updateObject, err => {
  // handle errors here
})
```
