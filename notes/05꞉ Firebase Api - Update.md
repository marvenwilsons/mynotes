---
tags: [Firebase]
title: '05: Firebase Api - Update'
created: '2020-06-10T17:48:54.379Z'
modified: '2020-06-10T18:14:46.632Z'
---

## 05: Firebase Api - Update
```js
import { firebaseAuth, firebaseDb } from 'firebase.js'
 
// get user uid, jane doe's id
const userId = firebaseAuth.currentUser.uid
 
// get tasks
const userTasks = firebaseDb.ref('/task', + userId)

userTasks.update(/** update object */, err => {
  // handle errors here
})
```
