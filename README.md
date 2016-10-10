# evrythng-webapp

Sample mobile web app that interacts with EVRYTHNG. Built with Web Components + Polymer + Material Design.

All requests are done locally if there is an EVRYTHNG Hub in the network and its address is configured correctly in the application.

Change Hub Address

Open up the application, logging in with any existing Facebook user.

Go to Settings and change the 'Local Hub Address' setting. This will be persisted locally, so the next time you open the application it will use that address by default.

#### Supported browsers

Browser support is basically the same as stated for Polymer ~1.*. All major evergreen browsers.

#### Deploy your application to github pages

##### Initial setup
- Ensure you have Bower and Polymer CLI installed (`npm i -g polymer-cli bower`)
- Ensure you repository is public and github pages are enabled
- Create gh-pages branch
- Run `polymer build`, ensure build folder created, with bundled (HTTP 1.1) and unbundled (HTTP 2) builds
- `git add build/bundled && git commite -m "Added built application to gh-pages"`

##### Deploy changes
- `polymer build`
- `git subtree push --prefix build/bundled origin gh-pages`