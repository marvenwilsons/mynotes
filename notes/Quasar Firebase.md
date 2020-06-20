---
tags: [Quasar]
title: Quasar Firebase
created: '2020-06-09T17:45:11.926Z'
modified: '2020-06-12T00:14:34.469Z'
---

# Quasar Firebase

## Step 1: Firebase project setup
#### Creating a firebase project and firebase database
- Note: Create a new firebase project if you do not have a project, head over to `firebase.google.com` else you can skip this step.
	
    - Click `Get Started` then choose a google account you want to login this also where the firebase will going to be associated.
    - You will be re directed to the google firebase dashboard, click `Add Project` and fill out the necessary information, accept the terms and clock create project.
    - create a realtime database, google offers two types of firebase databse, 1. cloud firestore, 2. realtime databse.
    - Choose `start in test mode` or `start in locked mode`

#### Enabling firebase Authentication
- Click `Authentication` in sidebar dashboard
- Click `Set up Sign In Method`
- Select the sign in providers then click `enable`

#### Adding App to firebase
On this section we will be adding an app to your fireabase project, by the end of this section firebase will generate a javascript object containing properties that is required to by your quasar app on communicating to your firebase project.
to enable firebase operations by using and accessing firebase database methods.

- first head over to `console.firebase.google.com`
- select and click the firebase project you want to add an app to
- click the `Add App` button, then an array of buttons will appear
- click `</>` to select the web setup
- fill the necessary information in the register app section, you can leave the `also set up Firebase Hosting` unchecked.
- click register app
	
    - a new section will appear call `Add Firebaase SDK` containing the essential properties to be use in communicating through the quasar app.
- you can now copy the config object in `Add Firebase SDK` section, or go back on it later after setting up quasar for firebase.

There you go! you have successfully created a `realtime database` and `enable  authentication` in your firebase database, and generated a `config object`

Next we will set up quasar for firebase operations.

## Step 2: Quasar firebase set up

#### Enabling App Authenticaion and installing firebase
Creating `Boot File` for firebase
-	first we have to create a boot file in quasar, we will use this boot file to put our `firebase instance`, `firebase cofigurations`, or connection strings and `firebase authentication`.
	- `$ quasar new boot firebase`
- next we have to reference or register the newly created `boot file` in `quasar.conf.js`
```js
// quasar.conf.js <-- file located in root dir
boot: [
	'firebase'
]
```
Installing firebase to quasar and configuring it

- first install firebase `$ npm install --save firebase`
- in your boot firebase file import firebase to configure
```javascript
// boot/firebase.js
import * as firebase from 'firebase/app'
import 'firebase/auth'
import 'firebase/database'

const firebaseConfig = {/** firebase config here */}
const firebaseAuthInstance = firebase.initializeApp(firebaseConfig)

const firebaseAuth = firebaseAuthInstance.auth()
const firebaseDb = firebase.database()


export { firebaseAuth, firebaseDb }
```

 
