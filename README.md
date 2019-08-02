# Boilerplate: Electron + Create React App + Electron Builder

A boilerplate to build an Electron app using Create React App and Electron Builder.

## Getting Started

### Directory Layout

```
.
├── /build/                         # The folder for compiled output
├── /node_modules/                  # 3rd-party libraries and utilities
├── /src/                           # The source code of the application
│   ├── /index.js                   # Startup script
│   └── /registerServiceWorker.js   # Lets the app load faster on subsequent visits in production
├── /public/                        # Static files which are copied into the /build/ folder
│   ├── /electron.js                # Startup script of your app, which will run the main process with Electron
├── .rescriptsrc.js                 # Wrap CRA configs with Rescripts
├── .webpack.config.js              # Customize webpack configuration created with CRA
└── package.json                    # The list of 3rd party libraries and utilities
```

### How to Install

```shell
$ yarn install
```

This will install both run-time project dependencies and developer tools listed in package.json file.

### How to Start

```shell
$ yarn electron-dev
```

This command will build the app from the source files (`/src`) into the output `/build` folder.
As soon as the initial build completes, it will start a light-weight developer server.

Now you can open your web app in a browser and start hacking.
Whenever you modify any of the source files inside the /src folder, the module bundler (Webpack)
will recompile the app on the fly and refresh all the connected browsers.

Note that the npm start command launches the app in development mode, the compiled output files are not optimized
and minimized in this case. For more information, check out the additional documentation.

### How to Package

Run this command to package the app:

```shell
$ yarn electron-pack
```

This command builds the app for production to the dist folder.
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.
By default, it also includes a service worker so that your app loads from local cache on future visits.

### Additional Scripts

* `"postinstall": "electron-builder install-app-deps"` - will ensure that your native dependencies always match the electron version.
* `"preelectron-pack": "yarn build"` - will build the CRA.
* `"electron-pack": "electron-builder -w"` - is used to build Electron app for Windows. See more information [here](https://www.electron.build/multi-platform-build).

### References

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

#### Included dependencies:

* [electron](https://electronjs.org) - build cross platform desktop apps with JavaScript, HTML, and CSS.
* [electron-builder](https://github.com/electron-userland/electron-builder) - build a ready for distribution Electron app with “auto update” support out of the box.
* [react](https://github.com/facebook/react) - library for building user interfaces.
* [rescripts](https://github.com/harrysolovay/rescripts) - take control of your create-react-app project configurations.
* [react-scripts](https://github.com/facebook/create-react-app) - create React apps with no build configuration.
* [react](https://github.com/facebook/react) - library for building user interfaces.
