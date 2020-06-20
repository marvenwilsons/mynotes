---
tags: [Donque CMS]
title: diwn
created: '2020-06-09T19:50:37.235Z'
modified: '2020-06-09T19:50:51.675Z'
---

## diwn

## dwin top

Spawns a top bar view
```js
dwin.spawn({
    section: 'top',
    winView: 'raw',
    winConfig: {},
    viewConfig: {},
    data: {
        name: 'foo',
        age: 30
    }
}, (event,context,close) => {
    context.set('data', {
        name: 'marven',
        age: '28'
    }).then(() => {
        close()
    })
})
```

## dwin right

Spawns a side bar view
```js
dwin.spawn({
    section: 'top',
    winView: 'raw',
    winConfig: {},
    viewConfig: {},
    data: {
        name: 'foo',
        age: 30
    }
}, (event,context,close) => {
    context.set('data', {
        name: 'marven',
        age: '28'
    }).then(() => {
        close()
    })
})
```
