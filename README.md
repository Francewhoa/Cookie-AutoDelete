[![Build Status](https://travis-ci.org/Cookie-AutoDelete/Cookie-AutoDelete.svg?branch=2.X.X-Branch)](https://travis-ci.org/Cookie-AutoDelete/Cookie-AutoDelete)
[![Coverage Status](https://coveralls.io/repos/github/mrdokenny/Cookie-AutoDelete/badge.svg?branch=master)](https://coveralls.io/github/mrdokenny/Cookie-AutoDelete?branch=master)
[![Crowdin](https://d322cqt584bo4o.cloudfront.net/cookie-autodelete/localized.svg)](https://crowdin.com/project/cookie-autodelete)
# Cookie-AutoDelete
Control your cookies! This extension is inspired by Self Destructing Cookies. When a tab closes, any cookies not being used are automatically deleted. Prevent tracking by other cookies and add only the ones you trust. Easily import and export your Cookie Whitelist.

## Main Features
- Auto Deletes Cookies from Closed Tabs
- WhiteList/GreyList Support for Cookies
- Easily Export/Import your Whitelist
- Clear All Cookies for a Domain
- Supports Manual Mode Cleaning from the popup
- Easily See the Number of Cookies for a site
- Support for Container Tabs (Firefox 53+ Only)

### Usage
1. Add the sites you want to keep cookies in the WhiteList (permanently) or GreyList (until Browser restart)
2. Enable "Active Mode" in the popup or settings
3. Watch those unused cookies disappear :)

## Other Versions
[Chrome](https://chrome.google.com/webstore/detail/cookie-autodelete/fhcgjolkccmbidfldomjliifgaodjagh)

[Firefox](https://addons.mozilla.org/en-US/firefox/addon/cookie-autodelete/)

### Contributing

#### Internationalization (i18n)

[Translate Cookie AutoDelete in your language or help fix a translation on Crowdin!](https://crowdin.com/project/cookie-autodelete)

#### Contributing Code

##### Requirements
- Bash (cause there's some .sh scripts otherwise you can't do `npm run build` but can still do `npm run dev`)
- Latest version of nodejs

##### Development
- `npm install` - Installs all dependencies
- `npm run dev` - This will run the webpack watcher and automatically pack `/src/background.js` and its dependencies to `/extension`
- `npm run lint` - Runs the eslinter for js files
- `npm test` - Runs the test suite located in `/test`
- `npm run build` - Builds the Firefox (.xpi) and Chrome (.zip) Builds

##### Testing
1. Run `npm install` (if you haven't already)
2. Run `npm run dev`
3. Load the extension in the browser

- Firefox
  - Easiest way would be to run the tool [web-ext](https://developer.mozilla.org/en-US/Add-ons/WebExtensions/Getting_started_with_web-ext#Testing_out_an_extension)
  - Another way is go into `about:debugging` and load `/extension/manifest.json`

- Chrome
  - In the extension tab, enable Developer Mode, then `load unpacked extension` and load the `/extension` folder

##### Building

1. Run `npm install` (if you haven't already)
2. Run `npm run build`
3. The build files should be in a new folder called `/builds`
