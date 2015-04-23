# jquery-breaks-angular-material
Project showing how inclusion of jquery breaks angular-material when using es6 and jspm.

# Installation

Clone from git.

**NOTE: Make sure gulp and jspm are installed globally, e.g. npm install -g gulp jspm**

Run `npm install`

Run `jspm install`

# Running

Run `gulp`

Navigate to: http://localhost:8080/index.html

Everything works fine. Angular loads a module (angular-material) and page renders correctly. Import of jquery is commented out.

Now, navigate to http://localhost:8080/index-bad.html.

Notice stack/error trace in browser console. Angular app is not loaded.  By simpling importing jquery into `.js` file, the app breaks.

Here is the 1-line change:
```javascript
import $ from 'jquery';
```
