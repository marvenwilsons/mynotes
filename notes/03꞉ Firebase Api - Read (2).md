---
tags: [Firebase]
title: '03: Firebase Api - Read'
created: '2020-06-09T21:03:31.360Z'
modified: '2020-06-10T18:18:22.758Z'
---

## 03: Firebase Api - Read

Lets say, we have a set of data in your firebase database associated with users, the set of data below represents users with their collections of task.

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

## Reading firebase database
To reach and read your firebase database data, firebase required the exact name of the database you want to read from then the exact name of the collection and a user id.

```javascript
import { firebaseAuth, firebaseDb } from 'firebase.js'

// get user uid, jane doe's id
const userId = firebaseAuth.currentUser.uid

// get tasks
const userTasks = firebaseDb.ref('/task', + userId)

// initial read to database
userTasks.once('value', snapshot => {
  // ....
}, err => {
  // handle err here
})


// hook, get each tasks
// the hook child_added will fire anytime there is a new node added, 
// and when first connecting to database
userTasks.on('child_added', snapshot => {
  const task = snapshot.val() // <-- individual task
})

// hook will fire ayntime when an existing node is changed or updated
userTasks.on('child_changed', snapshot => {
  const task = snapshot.val() // <-- individual task
})

// hook will fire ayntime when a node is deleted
userTasks.on('child_removed', snapshot => {
  const task = snapshot.val() // <-- individual task
})
```
