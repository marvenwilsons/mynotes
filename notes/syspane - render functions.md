---
tags: [Donque CMS]
title: syspane - render functions
created: '2020-06-09T19:48:47.896Z'
modified: '2020-06-09T20:57:07.111Z'
---

## syspane - render functions

### Methods
`render` `getServiceView` `renderPane`

## syspane.render(dataSet,viewIndex,beforeRender)
- void
- `dataSet:` string | number | Object | Array
- `viewIndex:` number | null | undefined
- `beforeRender:` Function | null | undefined

Adds a new pane to the pane's array and renders it using
the dataSet as the condition on running the `views` Function.

this function uses `syspane.renderPane()` and `syspane.getServiceView()` functions. 

Example: Common Usage
```js
syspane.render('foo')
```

Example: with `viewIndex`
```js
// viewIndex if null or undefined will be defualt to 0
syspane.render('foo',1)
```

Example: with `beforeRender`, this function executes after the `dataSet` is assigned a view and before constructing a `paneObject`.

`beforeRender` gives the user power to extend or trim the `dataSet` but with using the same view.
```js
syspane.render('foo',null, (dataSet) => {
	// do some dataSet validation and mutation
    // it is important to return something at the end to avoid null values on paneData
    return dataSet
})
```
Example: using promise
```js
syspane.render('foo',null, (dataSet) => {
	// do some dataSet validation and mutation
    // it is important to return something at the end to avoid null values on paneData
    return new Promise((resolve,reject) => {
    	setTimeout(() => {
            dataSet.name = 'Jane Doe'
        	resolve(dataSet)
        },100)
    })
})
```


## syspane.getServiceView(dataSet,viewIndex)
- returns: `paneObject` file content
- `dataSet:` string | number | Object | Array
- `viewIndex:` number

Constructs a `paneObject` using `dataSet` provided by executing the `views` function in the `serviceObject`

## syspane.renderPane(paneObject,paneIndex,viewIndex)

This function is not available in the service file and its not advisable for normal usage, use `syspane.render` instead

- void
- `paneObject:` Object
- `paneIndex:` number
- `viewIndex:` number

Renders a new pane
