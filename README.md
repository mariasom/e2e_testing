# Introduction into E2E testing

## warning! work in progress!

This project should serve as introduction into e2e testing for web based applications using [webdriverIO](https://webdriver.io/) framework.

Examples will be shown on simple web site: [the-internet.herokuapp](https://the-internet.herokuapp.com/).

## Tools

```plain
Webdriver I/O   https://webdriver.io/
Mocha           https://mochajs.org/
Chai            https://devhints.io/chai
NodeJS          https://nodejs.org/en/
TypeScript      https://www.typescriptlang.org/
```

### Webdriver I/O

```plain
Documentation   https://webdriver.io/docs/
Javascript API  https://webdriver.io/docs/api.html
```

### Useful links 
```plain 
CSS Selectors   https://www.w3schools.com/cssref/css_selectors.asp
```

## Install dependencies

```sh
npm install
```

### Setting up configuration

configuration file `conf.json` can contain:
For performance reasons don't set `maxInstances` above 4 unless you have powerful machine.

```json
{
    "baseUrl": "",      // app url
    "headless": "",     // boolean
    "junit": "",        // boolean 
    "maxInstances": "", // number of instances
    "remoteHost": "",   // ip of selenium hub
    "downloadDir": "",  // directory where test saves files
    "logLevel": "",     // trace | debug | info | warn | error | silent
    "firefox": true,    // specify browser, where tests should be executed
    "chrome": true,     
    "edge": true,       
    "safari": true,     
}
```

## Run e2e tests

### Basics

Run all tests on local machine

```sh
npm run test
```

Run specific test

```sh
npm run test -- --spec ./test/test_name.spec.ts
```

Run specific suite

```sh
npm run test -- --suite suite_name

```

