---
tags: [Firebase]
title: '06: Firebase Api - Remove'
created: '2020-06-10T17:55:08.752Z'
modified: '2020-06-10T18:15:09.191Z'
---

## 06: Firebase Api - Remove

```js
import { firebaseAuth, firebaseDb } from 'firebase.js'
 
// get user uid, jane doe's id
const userId = firebaseAuth.currentUser.uid
 
// get tasks
const userTasks = firebaseDb.ref('/task', + userId)

// removes the node that is being reference
userTasks.remove(err => {
  // handle errors here
}) 
```
