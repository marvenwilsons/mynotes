---
tags: [Donque CMS]
title: syspane - prompt functions
created: '2020-06-09T20:51:52.166Z'
modified: '2020-06-09T20:53:07.133Z'
---

## syspane - prompt functions

## syspane.prompt()
methods available in```paneOnLoad()``` hook
in listify
#### .prompt([promptObject],[callback])

#### type slider - string
spawns a text-field pane modal
```js
syspane.prompt({
    type: 'string',
    header: 'Sample Header',
    info: 'infomsg', // can be null
    error: null  // error message string on prompt load
    isClosable: false, // if null defaults to true
}, (input,progress,error) => {
    if(input == undefined) {
        error('Page Name is required')
    } else {
        // using progress is optional
        progress('starting')
        setTimeout(() => {
            progress('validating input', 3)
            setTimeout(() => {
                progress('processing 2')
                setTimeout(() => {
                    progress('updating pane data',syspanemodal.close)
                }, 500);
            }, 1000);
        }, 500);
    }
})
```

#### type: slider
spawns a number slider input pane modal
```js
syspane.prompt({
    type: 'slider',
    header: 'Sample Header',
    value: {
        min: 10,
        max: 90
    },
    defaultValue: 20, // can be null
    info: 'this is an info msg', // can be null
    error: null,  // error message string on prompt load
    isClosable: false, // if null defaults to true
}, (input,progress,error) => {
    if(input < 10) {
        error('input is invalid')
    } else {
        // using progress is optional, I use setTimeout to simulate aync operations
        progress('starting')
        setTimeout(() => {
            progress('validating input', 3)
            setTimeout(() => {
                progress('processing 2')
                setTimeout(() => {
                    progress('updating pane data',syspanemodal.close)
                }, 500);
            }, 1000);
        }, 500);
    }
})
```
#### type slider - minmax
spawns a range slider pane modal
```js
syspane.prompt({
    type: 'minmax',
    header: 'Sample Header',
    value: {
        min: 1,
        max: 100
    },
    defaultValue: [20,70],  // can be null
    info: 'this is an info msg', // can be null
    error: null,  // error message on prompt load
    isClosable: false,
}, (input,progress,error) => {
    if(input[0] > 20) {
        error('Invalid min value')
    } else {
        // using progress is optional, I use setTimeout to simulate aync operations
        progress('starting')
        setTimeout(() => {
            progress('validating input', 3)
            setTimeout(() => {
                progress('processing 2')
                setTimeout(() => {
                    progress('updating pane data',syspanemodal.close)
                    console.log(input)
                }, 500);
            }, 1000);
        }, 500);
    }
})
```

#### type slider - number
spawns a text-field pane modal
```js
syspane.prompt({
    type: 'number',
    header: 'Sample Header',
    defaultValue: null,  // type number, can be null
    info: 'this is an info msg', // can be null
    error: null,  // error message on prompt load
    isClosable: false,
}, (input,progress,error) => {
    if(input == undefined) {
        error('input is required')
    } else {
        progress('starting')
        setTimeout(() => {
            progress('validating input', 3)
            setTimeout(() => {
                progress('processing 2')
                setTimeout(() => {
                    progress('updating pane data',syspanemodal.close)
                    console.log(input)
                }, 500);
            }, 1000);
        }, 500);
    }
})
```
#### type slider - select
spawns a select pane modal
```js
syspane.prompt({
    type: 'select',
    header: 'Sample Header',
    value: ['foo','bar'],
    defaultValue: 'bar', // can be null
    info: 'this is an info msg', // can be null
    error: null,  // error message string on prompt load
    isClosable: false, // if null defaults to true
}, (input,progress,error) => {
    if(input < 10) {
        error('input is invalid')
    } else {
        // using progress is optional, I use setTimeout to simulate aync operations
        progress('starting')
        setTimeout(() => {
            progress('validating input', 3)
            setTimeout(() => {
                progress('processing 2')
                setTimeout(() => {
                    progress('updating pane data',syspanemodal.close)
                }, 500);
            }, 1000);
        }, 500);
    }
})
```
#### type slider - multiselect
spawns a multiselect pane modal
```js
syspane.prompt({
    type: 'multiselect',
    header: 'Sample Header',
    value: ['foo','bar','fizz'],
    defaultValue: ['bar'], // can be null
    info: 'this is an info msg', // can be null
    error: null,  // error message string on prompt load
    isClosable: false, // if null defaults to true
}, (input,progress,error) => {
    if(!input) {
        error('input is invalid')
    } else {
        // using progress is optional, I use setTimeout to simulate aync operations
        progress('starting')
        setTimeout(() => {
            progress('validating input', 3)
            setTimeout(() => {
                progress('processing 2')
                setTimeout(() => {
                    progress('updating pane data',syspanemodal.close)
                }, 500);
            }, 1000);
        }, 500);
    }
})
```
#### type slider - password
```js
paneMethods.prompt({
    type: 'password',
    header: 'Enter Password',
}, (input,progress,error) => {
	// encrypt password or validate format here
    // send to server
    if(!input) {
        error('input is invalid')
    } else {
        // using progress is optional, I use setTimeout to simulate aync operations
        progress('starting')
        setTimeout(() => {
            progress('validating input', 3)
            setTimeout(() => {
                progress('processing 2')
                setTimeout(() => {
                    progress('updating pane data',syspanemodal.close)
                }, 500);
            }, 1000);
        }, 500);
    }
})
```

