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

### Demo

A demo version of this Web app is deployed on: https://connected-demo.evrythng.com/
or scan:

![Alt text](https://tn.gg/jEXRpN43.qr)

Note that you'll be prompted for a valid EVRYTHNG Trusted App Key.

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

You can deploy the app on any server such as GitHub pages but here are some examples

### To Netlify
1. Login at netlify.com
2. Go to the Netlify [dashboard](https://app.netlify.com/)
3. Click 'Add a new project'
4. Choose 'GitHub'
5. Select the forked 'evrythng-connected-app' repository
6. Fill in the following fields: 
  - branch: `master` 
  - public folder: `build/bundled`
  - build command: `npm i polymer-cli -g && polymer build`
7. Click 'Create'
8. Wait until first build is finished
9. Enjoy and redeploy on every push to `master`


