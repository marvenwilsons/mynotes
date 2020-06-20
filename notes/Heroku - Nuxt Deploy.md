---
tags: [Heroku]
title: Heroku - Nuxt Deploy
created: '2020-06-09T19:25:09.491Z'
modified: '2020-06-09T19:33:11.346Z'
---

## Heroku - Nuxt Deploy

1. Create a new app in heroku then follow the doc of heroku deploy upon creating the new app
2. Set heroku config, go to settings scroll down and click `Reveal Config Vars` then add.
	- `HOST= 0.0.0.0`
    - `NODE_ENV= production`
    - `NPM_CONFIG_PRODUCTION= false`
3. Add `"heroku-postbuild": "npm run build"` on scripts object in package.json file
4. commit changes and push using `git push heroku master`
