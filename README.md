# Welcome to the Salesfy Project

Salesfy was a project developed by me and my partners to solve the problem of sales/channel enablement in Brazil. This project no longer exists, as we headed our lives to some other objectives. Even if we don't work at it anymore, the code is here.

The project is divided into three parts: Backend, Frontend and Shared. Shared was our intermediate project which contained the business code and utilities that is used both by Backend and Frontend - as we did not want any duplicated logic. I (github.com/taranto) developed every single line of the Backend, Shared and most part of Test-Web project. They're all here in github for you to see.

As I've dived into Typescript just after leaving Java, some old archieves may be a little javaish until more functional programming started to go on. Some other routes flow started to get a cleaner code as I had time to build up a more consistent architecture. It had happen because primarily I needed to make my business live, only then I was able to do a non-verbose code. 

Some verbose code are still there as they were already working bug-free and as I had all tests automated. At that time it was better to develop a new feature than spend time wiping up code. It would be better to wait until something were supposed to be done in those archieves to make a better code of it.

Maybe a Sales/Channel enablement new project may not exacly start from this project here, but the built up architecture may fast forward any project as it has many things already implemented (and some routes samples there to be seen as a exemple).

I hope you can make the best of use :)

### INSTALLATION requirements:
* postgres 9.6.11
* nvm
* node 9.11.2
* npm 5.6.0
* yarn
* vscode

### INSTALLING SHARED PROJECT:

```sh
git clone https://github.com/taranto/salesfy-shared.git
yarn reinstall
yarn compile
yarn test
```

### INSTALLING DATABASE:

in the folder you cloned shared, clone backend project by it's side:

`git clone https://github.com/taranto/salesfy-backend.git`

run in your database all code from the archieve `SQL changes.sql` and `SQL test env.sql`

### INSTALLING BACKEND PROJECT:

into the salesfy-backend folder, duplicate the archieve `config.env.template` and rename it to `configTest.env`. Replace the unfilled keys.
`DB_` prefix are the ones for your database. `EMAIL_` prefix handles your email. `LOGIN_` and `S3_` are very specific, but not really necessary now. 

into the salesfy-backend folder, run:
```sh
$ yarn full-reinstall
$ yarn compile
$ yarn online
```

add an user to the database quickly with the command: `yarn use-quick-register`

shut down your online status, then:

`yarn test`

### INSTALLING FRONTEND PROJECT:

in the folder you cloned shared, clone frontend project by it's side:

`git clone https://github.com/taranto/salesfy-frontend.git`

*the app is not being able to install/work right now (only the web)

`yarn full-reinstall`

-Run the Backend project (`yarn online`)

`yarn web-dev`

### INSTALLING TEST-WEB PROJECT:
in the folder you cloned shared, clone test-web project by it's side:
`https://github.com/taranto/salesfy-test-web.git`
* Find your chrome version (usually at help -> about google chrome)
* Find your chromedriver version compatible with your chrome: https://sites.google.com/a/chromium.org/chromedriver/downloads
*Actually the chromedriver's 2.38 version (the one commited) is associated to the version 65.0.3325.181 (official build) (64-bit) of chrome browser. It works well for the version 83.0.4103.39 of chrome browser (current version of 25/05/2020). If it doesn't work well, run `npm uninstall chromedriver` and `npm install chromedriver@xxx --save` switching `xxx` with the correct version.

`yarn full-reinstall`

`yarn compile`

* Switch the email/password of the test user according to your database (at src/Env.ts)
* Run the Backend project (`yarn online`)
* Run the Frontend project (`yarn web-dev`)
* Run this test project (`yarn test`)

*As soon as this project test runs, the chorme browser will open up by itself and a series of mouse clicks and keyboard types would start to be made automatically.
