---
tags: [Donque CMS]
title: syspane - update functions
created: '2020-06-09T19:51:52.902Z'
modified: '2020-06-09T20:58:00.804Z'
---

## syspane - update functions

## updatePaneData(objData,targetKey)
- void
- `objData:` string | number | Object | Array
- `targetKey:` string | null | undefined

Updates the paneData in the current pane

Example: Common Usage
```js
syspane.updatePaneData('foo')
```

Example: With `targetKey`

let say we want to update a property inside this object: `{name: {firstName: 'Ann Doe' } }`

```js
// updating firstName to Jane Doe
syspane.updatePaneData('Jane Doe', 'name.firstName')
```

## updateTargetPaneData(pi,objData,targetKey)
- void
- `pi - paneIndex:` number
- `objData:` string | number | Object | Array
- `targetKey:` string

## updateChildPaneData(objData,targetKey)
- void
- `objData:` string | number | Object | Array
- `targetKey:` string

## updateParentPaneData(objData,targetKey)
- void
- `objData:` string | number | Object | Array
- `targetKey:` string
