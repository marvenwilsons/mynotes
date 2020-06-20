---
tags: [Heroku]
title: Heroku - puppeteer
created: '2020-06-09T19:23:47.740Z'
modified: '2020-06-09T19:34:04.273Z'
---

Heroku - puppeteer

## Setting View port
```js
// set view port 
page.setViewPort({widthL 1280, height: 800})
```

## Adding buildpack to heroku application
pupperteer cannot run in production without installing linux
build packs.
- github - https://github.com/jontewks/puppeteer-heroku-buildpack
- youtube - https://www.youtube.com/watch?v=Kl7mqpAK-bk
