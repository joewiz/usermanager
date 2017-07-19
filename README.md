# eXistdb User Manager app

Rewrite of original user manager used to be deployed as plugin of the 
eXistdb dashboard.

This new version is based upon Web Components specifically on Polymer 2.0 for cross-browser compat.

UserManager 2 comes as a standalone application and is not dependent on dashboard any more.

This is still an early release. There are certainly some detail issues. Help, comments and proposals welcome. 

## Setup 

This app requires NodeJS and [Polymer CLI](https://www.polymer-project.org/2.0/start/toolbox/set-up) for creating
optimized builds of the application. For development purposes you can simply call ```ant``` to create a xar.

1. make sure you have NodeJS installed. See 'notes on setting up nodejs' below for help.
1. execute ```npm install``` to load dependencies
1. excecute ```polymer``` to make sure you have Polymer CLI installed (should be 1.3.1 or up). If you need to install it first
 execute ```npm install -g polymer-cli```
1. execute ```bower install```

## tooling

If you have installed NodeJS you can make use of following gulp commands:

```gulp watch``` - will watch your local files and auto-deploy to the db when changed.
```gulp deploy``` to push all local files to the db.

Note: you must have installed the xar application once in the database before running these commands. gulp will not
create the app in the db itself but just update it if it's there.

## building

To create an optimized build execute:

```ant production-xar```


## Notes on setting up nodejs

Note: This is a one-timer - you can skip this step if you got mpm on your system already.

Though not strictly required for development it is recommended that you have an installation of nodejs on your system.
It is recommended to use ['nvm'](https://github.com/creationix/nvm) to install nodejs as this eases the process of installation and 
allows to keep different versions of it on your system without conflicts.

Nodejs is used within this project to drive the gulp tasks and handle client-side dependencies with bower.
 
Please refer to the nvm page for installation instruction or use an installation method described
on the nodejs.org homepage.

