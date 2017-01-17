# EVRYTHNG Sample Web App

This project is a sample mobile web app that interacts with the [EVRYTHNG API](https://developers.evrythng.com/) as well as the [THNGHUB](https://developers.evrythng.com/docs/thng-hub) local gateway. 
It was built with Web Components + Polymer + Material Design.

All requests are done locally if there is an EVRYTHNG THNGHUB in the network and its address is configured correctly in the application.

## Setup

### Prerequisites
For this app to work you'll need:
1) An EVRYTHNG account
2) To have created an EVRYTHNG app in your account
3) Have either Facebook login activated for your EVRYTHNG app, or a valid App User's credentials (email + password)

### Changing the THNGHUB Address

Go to Settings and change the 'Local Hub Address' setting. This will be persisted locally, so the next time you open the application it will use that address by default.

## Building the App

Ensure you have Bower and Polymer CLI installed: 
```
npm i -g polymer-cli bower
```
Install the dependencies:
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

## Deploying to GitHub pages
- Ensure you repository is public and github pages are enabled
- Create gh-pages branch
- Run `polymer build`, ensure build folder created, with bundled (HTTP 1.1) and unbundled (HTTP 2) builds
- `git add build/bundled && git commit -m "Added app to gh-pages"`

### Deploying changes
- `polymer build`
- `git subtree push --prefix build/bundled origin gh-pages`

## Supported browsers
Browser support is basically the same as stated for Polymer ~1.*. All major evergreen browsers.
