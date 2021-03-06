As a part of making Hygieia more modular, this repo will host Hygieia UI code. More to come!!!!

# Hygieia UI
[![Build Status](https://travis-ci.com/Hygieia/UI.svg?branch=master)](https://travis-ci.com/Hygieia/UI?branch=master)
[![Maven Central](https://img.shields.io/maven-central/v/com.capitalone.dashboard/UI.svg?label=Maven%20Central)](https://search.maven.org/search?q=g:%22com.capitalone.dashboard%22%20AND%20a:%22UI%22)
[![Total alerts](https://img.shields.io/lgtm/alerts/github/Hygieia/UI.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/Hygieia/UI/alerts/)

This project requires Angular CLI version 8.0.3.
This project requires java version : openjdk version "1.8.0_265"

## Setup:
1. Fork and clone the UI folder
2. Navigate to your UI folder and install the package dependencies by running `npm install`
3. Download Angular CLI by running `npm install -g @angular/cli@8.0.3`
4. You can run `ng version` to check your Angular CLI version and related package dependency versions (make sure the package versions are v8)

## Build and run the executable file for the api 

Before you start, you must run the api on the side.  After you fork/clone the Hygieia [api](https://github.com/Hygieia/api), navigate to the `\api` directory and run the following command: 

`mvn clean install` 

This will create an output `api.jar` file in the `\target` folder.  

Tip: Before you continue, make sure you set the configurable parameters in the api.properties file to connect to the dashboard MongoDB database instance, including properties required by the API module.  For more information, please visit the [Hygieia api guide](https://hygieia.github.io/Hygieia/api.html). 

Navigate to `api\target,` and execute the following command in the command prompt: 

`java -jar api.jar --spring.config.location=C:\[path to api.properties file] -Djasypt.encryptor.password=hygieiasecret`

## Build the Project
With the api running, open a different terminal and run `ng build` in your \UI folder. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build. 

## Building  the Project and launching the dashboard in Ubuntu (20.04) : Refer here for Ubuntu 20.04 
Versions of node and npm used => node version v12.18.3 , npm version  6.14.6 

In the UI/ folder :

Install gulp using command : npm install -g gulp 

To check the version : gulp -v 

You then have to install gulp locally on a per-project basis :  npm install gulp --save-dev

*If gulp is listed in the package.json (Under the UI folder) under 'dependencies' , then replace '--save-dev' with just '--save' 

With the api running, open a different terminal and run `gulp build` in your \UI folder. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build. 

To launch the dashboard : In the same UI/ folder run the command : gulp serve 


## Development server

In the \UI folder, run `ng serve` for a dev server. Navigate to `http://localhost:4200/` in a incognito browser. The app will automatically reload if you change any of the source files.
 
## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).  You can also debug using Karma.

An alternative method to run unit tests is to run `npm run test-headless` in your UI folder in a terminal.  This will also test your code coverage. 

## Debugging with IntelliJ

If you are using IntelliJ, you can debug with JavaScript Debug.  Navigate to the `Edit Configurations` tab, hit the + sign to `Add New Configuration,` and add `JavaScript Debug.`

Inside the `Run/Debug Configurations` popup, you can edit the name to your preference and change the URL to `http://localhost:4200.`  This will allow you to navigate the UI on localhost to hit the debug breakpoints you set.

Use the Default Chrome browser and apply your changes.

Note: When you start the debug property, it will open a new browser popup for debugging specifically (also in localhost:4200).

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).
