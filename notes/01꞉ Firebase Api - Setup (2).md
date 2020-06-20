---
tags: [Firebase]
title: '01: Firebase Api - Setup'
created: '2020-06-09T21:05:51.899Z'
modified: '2020-06-10T21:35:26.400Z'
---

## 01: Firebase Api - Setup

Installing firebase to quasar and configuring it

- first install firebase `$ npm install --save firebase`
- in your boot firebase file import firebase to configure
```javascript
// firebase.js
import * as firebase from 'firebase/app'
import 'firebase/auth'
import 'firebase/database'

const firebaseConfig = {/** firebase config here */}
const firebaseAuthInstance = firebase.initializeApp(firebaseConfig)

const firebaseAuth = firebaseAuthInstance.auth()
const firebaseDb = firebase.database()


export { firebaseAuth, firebaseDb }
```
