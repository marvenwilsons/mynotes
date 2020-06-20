---
tags: [General Notes]
title: Javascript Notes
created: '2020-06-14T06:03:04.232Z'
modified: '2020-06-14T06:12:57.137Z'
---

Javascript Notes

## File Upload and file to base64
Get file data in file upload, and get a base64 version of it.

Vue Html
```Html
 <input @change="fileSelect" id="imgfileinput" type="file">
 <img id="preview" />
```
Javascript
```js
methods: {
  fileSelect(e) {
    const file = e.target.files[0]
    const reader = new FileReader()
    const preview = document.getElementById('preview')

    reader.addEventListener("load", function () {
      // convert image file to base64 string
      preview.src = reader.result
    }, false);

    if(file) {
        reader.readAsDataURL(file)
    }

  }
}
```
