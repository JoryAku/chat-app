Chat App 
===
Ember.js 2.3 tutorial
--

## Contents

### Session 1
Basics of Node.js and Ember.js

* [The best way to install Node.js](http://yoember.com/nodejs/the-best-way-to-install-node-js/) (link to yoember.com)
* [About package managers (npm, bower)](#user-content-package-managers)
* [Prerequisites for developing and running an Ember.js app](#user-content-prerequisites)
* [Installation of Ember CLI](#user-content-install-ember-cli)
* [Creating our first Ember application](#user-content-new-app)
* [Install Ember Inspector in Chrome/Firefox](#user-content-inspector)
* What is the add-on ecosystem around Ember.js? 
* [The best way to add Bootstrap to an Ember project](http://yoember.com/#ember-bootstrap-sass) (link to yoember.com)
* Ember.js router
* [Adding a navigation bar and About page to our project](#user-content-navigation-bar)
* Computed properties and observers

### Session 2

* WIP
* WIP


---



### Session 1

#### <a name='package-managers'></a>Package managers (node, bower)

`npm` is Node.js' package manager. It organises all dependencies in `package.json` file. In Ember.js project we use Node.js and `npm` for keeping our development process smooth and automatic, however, when you deploy your project, it will be only html, javascript, stylesheets and assets, like images and fonts. For example node packages help to combine your final project, but they won't be fully part of your concatenated application.

`npm` command line tool comes with Node.js. You can check out your version with `npm -v` and you can update with `npm install -g npm`. The `-g` means, this package will be global, so you can run it from every directory on your computer.

Important commands:

```
$ npm install
$ npm update
```
Learn more about `npm` here:

* [Getting started guide](https://docs.npmjs.com/getting-started/what-is-npm)
* [Package directory](www.npmjs.com)

`bower` is a package manager for assets. We use `bower.json` for listing javascript libraries and css frameworks, which need to run our frontend app when we publish. So these packages will be combined inside our final codebase. For example Bootstrap, jQuery, D3.js libraries will appear in this list if we need them.

Install bower:

```
npm install -g bower
```

* [More about Bower](http://bower.io/)

Luckily in Ember.js development, we don't really have to directly manage these packages, because Ember CLI addons deal with all requirements.

## <a name='prerequisites'></a>Prerequisites for running an Ember.js app

You will need the followings properly installed on your computer. These help in development process.

* [Git](http://git-scm.com/)

Probably you already have `git` on your computer. (It comes with XCode on Mac, on Windows you can install it with [Git for Windows](https://git-for-windows.github.io/)) 

* [Node.js](http://nodejs.org/) (with NPM)

See above.

* [Bower](http://bower.io/)

See above.

```
npm install -g bower
```

* [PhantomJS](http://phantomjs.org/)

PhantomJS is a headless browser. Ember.js uses it for running tests.

```
npm install -g phantomjs
```

* (Optional) [Watchman](https://facebook.github.io/watchman/)

Watchman is a tool for watching changes in your project folder, it triggers a rebuild action when you modify something in your code. It helps in live-reloading during the development process. (Only on Mac and on Linux at the moment. Facebook promised a Windows version soon.)

More details about [Watchman Installation](https://facebook.github.io/watchman/docs/install.html#build-install)

On Mac:
```
$ brew update
$ brew install watchman
```

## <a name="install-ember-cli"></a>Install Ember CLI

Open your terminal and install the latest [Ember CLI](http://www.ember-cli.com/)

```
$ npm install -g ember-cli@beta
```

This will install or if you already had will update to the latest version

You can check it with
```
$ ember -v
```



## <a name="new-app"></a>Creating our first Ember application

```
$ ember new chat-app
```

It will create a new folder with the app name, download all npm and bower packages.

Navigate in your new app folder:
```
$ cd chat-app
```

Launch your app with `ember server` and open in your browser.

```
$ ember server
```

Open the following link: [http://localhost:4200](http://localhost:4200)

## <a name="inspector"></a>Install Ember Inspector Chrome Extension

Follow instructions on the [official guide](https://guides.emberjs.com/v2.3.0/ember-inspector/installation/).

## <a name="navigation-bar"></a>Create navigation bar and an About page

Firstly, read the instructions on our [Ember.js tutorial](http://yoember.com/#navigation-bar) page, about how can you create a navigation partial. Secondly, you can create also a new About page. (Follow steps in the [Ember.js tutorial](http://yoember.com/#about-page))
 
You can use this add-on to make Ember.js `link-to` compatible with Bootstrap: https://github.com/zoltan-nz/ember-bootstrap-nav-link 

```
ember install ember-bootstrap-nav-link
```
Don't forget to update `link-to` to `nav-link-to` in navigation bar. 

## <a name="computed-property"></a>Learn more about computed property and observers

You can practice if you follow our connected tutorial section. [Computed property and observers in Ember.js](http://yoember.com/#lesson-2)
