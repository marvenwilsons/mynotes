---
tags: [Donque CMS]
title: Service File
created: '2020-06-09T21:00:18.834Z'
modified: '2020-06-09T21:00:28.331Z'
---

## Service File

```js
const path = require('path')
const Templates = require(path.join(__dirname,'../../server/templates.js'))

module.exports = Templates.Service({
	name: 'service name',
    initialData: function(sql,fetch) {
    	
    },
    views: function(data,client,utils,Templates){
    	if(data){
        	// return a view object here
        } else {
        	// return a view object here
        }
    }
})
```

# The view object
```js
const viewObject = {
	paneConfig: {
    	paneName: 'Untitle pane',
    	paneWidth: '550px',
    	isClosable: true,
    	paneViews: ['comp1','comp2'], // vue component registered globally
    	defaultPaneView: 0, // paneView item index
    	paneData: 'foo', // any
    },
    componentConfig: {
    	// the configuration object for the selected paneView
        // it can return anything depends on the component
    },
    paneOnLoad: function(syspane,syspanemodal,dwin) {
    	// executes when the pane loaded
    },
    onModalData: function(syspane,syspanemodal,dwin) {
    	// executes only when a custom modal view submits data
    }
}
```
