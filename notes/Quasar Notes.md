---
tags: [Quasar]
title: Quasar Notes
created: '2020-06-09T17:48:46.608Z'
modified: '2020-06-10T03:45:36.578Z'
---

Quasar Notes
## Quasar CLI
#### Create a new quasar project
- `$ quasar create folder_name`
#### Create a new boot file, and setup.
a boot file, is a code that runs before the vue instance is created.
- `$ quasar new boot <file name>`
```js
    // quasar.conf.js
boot: [
  '<file name>'
]
```
#### Create a new store, and set up
- `$ quasar new store`
- register the newly created store to `src/store/index.js`

## Quasar add global vue components
- create new boot file: `quasar new boot <name>`
- `boot/<name>` : import vue components and register 

## Transition single Component
doc: https://v0-16.quasar-framework.org/components/transition.html
```js
<template>
  <transition
    appear
    enter-active-class="animated fadeIn"
    leave-active-class="animated fadeOut"
  >
    <!-- Wrapping only one DOM element, defined by QBtn -->
    <q-btn v-if="a" color="secondary" icon="mail">
      Email
    </q-btn>
  </transition>
</template>
```





## Transition Multiple Components
doc: https://v0-16.quasar-framework.org/components/transition.html
```javaScript
<template>
  <transition-group
      duration="9000"
      enter-active-class="animated bounceInUp"
      leave-active-class="animated bounceOutRight"
    >
      <!-- We wrap a "p" tag and a QBtn -->
      <p v-if="a" key="text">
         Lorem Ipsum
      </p>
      <q-btn
        v-if="a"
        key="email-button"
        color="secondary"
        icon="mail"
        label="Email"
      />
	</transition-group>
</template>
```



## Vue Navigation Guard
```javascript
// boot/navigation-guard.js

export default ({router}) => {
  router.beforeEach((to,from,next) => {
    if(true) {
      next('/userDashboard')
    } else {
      next('/loginPage')
    }
  })
}
```
