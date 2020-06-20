---
tags: [Donque CMS]
title: sysmodal
created: '2020-06-09T20:53:43.767Z'
modified: '2020-06-09T20:56:02.351Z'
---

## sysmodal

### Methods
`ask` `logerr` `loginfo` `prompt` `select` `loading`

#### .ask([askObject: Object],[cb:function])
```js
// no need to do this if you are in a service file, because it is
// already injected
import controlpanel from '@/apps/controlpanel/controlpanel'

// initiate in vue component that has helper mounted as a mixin
const {actions} = controlpanel(this)

actions.sysmodal.ask({
    question: 'are you sure you want to continue?',
    truthy: 'contimue',
    falsey: 'cancel'
}, (response,progress,close) => {
    if(response) {
        // do something
        progress('analyzing ...')
        setTimeout(() => {
            progress('processing', 2)
            progress('done',close)
        }, 1000);
    } else {
        close()
    }
})
```

#### .logerr([msg:String])
```js
// no need to do this if you are in a service file, because it is
// already injected
import controlpanel from '@/apps/controlpanel/controlpanel'

// initiate in vue component that has helper mounted as a mixin
const {actions} = controlpanel(this)

actions.sysmodal.logerr('This is an error message!')
```

#### .loginfo([msg:String])
Display a message info
```js
// no need to do this if you are in a service file, because it is
// already injected
import controlpanel from '@/apps/controlpanel/controlpanel'

// initiate in vue component that has helper mounted as a mixin
const {actions} = controlpanel(this)

actions.sysmodal.loginfo('This is an error message!')
```

#### .prompt([prompt:Object],[progress:Function],[closeModal:function])
can be use for prompting password field or normal text field
```js
// no need to do this if you are in a service file, because it is
// already injected
import controlpanel from '@/apps/controlpanel/controlpanel'

// initiate in vue component that has helper mounted as a mixin
const {actions} = controlpanel(this)

actions.sysmodal.prompt({
    defaultValue: 'John Doe',
    placeholder: 'enter name',
    label: 'Input your name',
    type: '' // default -> string, password
    err: 'this is a sample error',
    onSubmit(input,progress,close) {
        // do something
        console.log(input)
        progress('starting proccess ...'2)
        
        setTimeout(() => {
            progress('succesfully end process', close)
        }, 1000);
    },
    onCancel() {
        // do something
        console.log('canceling')
        controlpanel.actions.sysmodal.closeModal()
    }
})
```
#### .select([selectObject:Object],[progress:Function],[closeModal:function])
```js
// no need to do this if you are in a service file, because it is
// already injected
import controlpanel from '@/apps/controlpanel/controlpanel'

// initiate in vue component that has helper mounted as a mixin
const {actions} = controlpanel(this)

actions.sysmodal.select({
    options:['foo','bar','fizz'],
    defaultValue: 'foo',
    label: 'Select an option',
    onSubmit(input,progress,close) {
        // do something
        console.log(input)
        progress('starting proccess ...'2)
        
        setTimeout(() => {
            progress('succesfully end process', close)
        }, 1000);
    },
    onCancel() {
        // do something
        console.log('canceling')
    }
})
```
#### .loading([cb:function])
use to display progress of an operation
```js
// no need to do this if you are in a service file, because it is
// already injected
import controlpanel from '@/apps/controlpanel/controlpanel'

// initiate in vue component that has helper mounted as a mixin
const {actions} = controlpanel(this)

actions.sysmodal.loading((progress, header, close) => {
    header('Fetching package')
    progress('starting ...')
    setTimeout(() => {
        progress('p1',3)
        setTimeout(() => {
            progress('p2')
            setTimeout(() => {
                header('installing')
                setTimeout(() => {
                    progress('end', close)
                }, 1000);
            }, 500);
        }, 2000);
    }, 1000);
})
```


