---
tags: [Firebase]
title: 07 Firebase Api - Storage Bucket
created: '2020-06-11T01:33:20.258Z'
modified: '2020-06-11T04:10:07.726Z'
---

## 07 Firebase Api - Storage Bucket

```js
import { firebaseStorage } from 'firebase.js'
const storageRef = firebaseStorage.ref(`folderName/fileName`)

const task = storageRef.put(file)

task.on('state_changed',
  function error(err) {
    // handle error
  },
  function progress(snapshot) {
    // handle progress
  },
  function complete() {
    // handle on complete
  }
)
```
