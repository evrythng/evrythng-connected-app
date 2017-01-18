# EVRYTHNG Sample Web App for Connected Products

This project is a sample mobile web app that interacts with connected products using the [EVRYTHNG API](https://developers.evrythng.com/) as well as the [THNGHUB](https://developers.evrythng.com/docs/thng-hub) local gateway. 
It was built with Web Components + Polymer + Material Design.

All requests are done locally if there is an EVRYTHNG THNGHUB in the network and its address is configured correctly in the application.

## Setup

### Prerequisites
For this app to work you'll need:

- An EVRYTHNG account
- To have created an EVRYTHNG App in your account
- Have either Facebook login activated for your EVRYTHNG app, or a valid App User's credentials (email + password)

### Changing the THNGHUB Address

Go to Settings and change the 'Local Hub Address' setting. This will be persisted locally, so the next time you open the application it will use that address by default.

## Building the App

Ensure you have Bower and Polymer CLI installed: 
```
npm i -g polymer-cli bower
```
Install the dependencies:

> Note: If prompted, choose Polymer version 1.6.0 or above.

```
bower install
```
Build the app:
```
polymer build
```

## Running the App

```
polymer serve
```

## Supported browsers
Browser support is basically the same as stated for Polymer ~1.*. All major evergreen browsers.

## Deploying 

You can deploy the app on any server but here are a few examples:

### To GitHub pages
- Ensure you repository is public and github pages are enabled
- Create gh-pages branch
- Run `polymer build`, ensure build folder created, with bundled (HTTP 1.1) and unbundled (HTTP 2) builds
- `git add -f build/bundled && git commit -m "Added app to gh-pages"`
- `git subtree push --prefix build/bundled origin gh-pages`

### To Netlify
1. Login at netlify.com
2. go to [dashboard](https://app.netlify.com/)
3. click 'add a new project'
4. choose 'github'
5. select forked 'evrythng-webapp'
6. fill the fields: branch: `master`, public folder: `build/bundled`, build cmd: `npm i polymer-cli -g && polymer build`
7. Click 'create'
8. Wait till first build is finished
9. Enjoy and redeploy on every push to master


