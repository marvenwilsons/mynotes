---
tags: [Firebase]
title: '02: Firebase Api - Db User'
created: '2020-06-09T21:01:57.284Z'
modified: '2020-06-10T17:49:37.702Z'
---

## 02: Firebase Api - Db User
complete doc: https://firebase.google.com/docs/reference/js/firebase.auth.Auth

#### Methods
- `createUserWithEmailAndPassword`
- `signInWithEmailAndPassword`
- `onAuthStateChanged`
- `signOut`


Creating a new firebase database user
```javascript
import { firebaseAuth  } from 'boot/firebase

const email = 'test@test.com'
const password = 'password123'

firebaseAuth
  .createUserWithEmailAndPassword(email,password)
	.then(response => {/** do something */})	
  .catch(error => {/** do something */})
```
Login a user to firebase database
```javascript
import { firebaseAuth  } from 'boot/firebase

const email = 'test@test.com'
const password = 'password123'

firebaseAuth
  .signInWithEmailAndPassword(email,password)
	.then(response => {/** do something */})	
  .catch(error => {/** do something */})
```

Authentication hook
```javascript
import { firebaseAuth  } from 'boot/firebase

firebaseAuth
  .onAuthStateChanged(function(user) => {
    if(user) {
      // do something when a user is present or login
    } else {
      // do someting when a user is not present or logout
    }
  })
```

Logout a user to firebase database
```javascript
import { firebaseAuth  } from 'boot/firebase

firebaseAuth.signOut()
```

