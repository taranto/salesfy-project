# Welcome to the Salesfy Project

### Introduction

Salesfy was a project developed by my partners and I from 2017 until 2020 to solve a few pain points of sales/channel enablement in Brazil. We worked on it for a few years while we tried to provide knowledge, ramping up and cohesion through a playbook tool to salesmen and marketing teams. Although the project no longer exists, as everyone in the company staff decided to head their lives to some other objectives. Even if we don't work with it anymore, the code is available here.

### Motivation

440h per year are spent by salesperson on studies;
Every year more than 20% of sales teams got their personnel changed;
3 to 6 months of ramping up for every new salesperson on average;
20% of time spent by other team sales members trying help ramping up newcomers;
Only 50% of salespersons achieved their sales goals during the year (2018 data);
20% better results when sales teams and marketing teams are in sync;

### Objective

Our objective is to provide a strategy to empower the sales team providing content, data, and insight to better impact the clients. This way we could leverage faster sales through playbooks, knowledge management and sales enablement;

### Salesfy project in practice

Salesfy is meant to be used by sales teams, sales managers and marketing teams. It focuses on solving the pain of ramping up sales teams by bringing up specific knowledge to them through contents already established by older members of the teams. These team members would easily build playbooks using our tool, so not only the sales manager would teach his new employees faster, but also make marketing teams better connected with the established sales team.

### Brief story of this project

It all started as a project of a social network for innovative business ideas where people could write, share and contribute to each other’s project to be able to land better businesses. This project was called "Hatchers". Later on we noticed that we would not be able to survive on the market as a b2c as we first thought (b2c’s costs are high and take a long time to be profitable). With that in mind we decided to pivot it to a b2b sales enablement business as it would be able to sustain this business for the first few years. After this decision, the code chunks got migrated from a b2c social network business logic to a b2b sales enablement one.

### Awards achieved

During the lifetime of both these two projects, we were granted a few awards for their innovative approach. It helped us to continue to work hard towards the objective to fulfill a gap in the market whether it being for new business ideas or sales enablement. They were from both private and governmental sources, earning benefits like funding equity free, mentoring, courses and business network. A few of these awards are:
- "Sinapse da Inovação" Award 2017, among 2700 startups we ended up in the 100th shortlist award
- "Projeto Centelha" Award 2019. Among 1219 startups we ended up in the 28th shortlist award
- “Inovativa” award (twice)
- “Iguá Lab” acceleration award
- “Sebrae capital empreendedor” award

### Project divisions

The programming part of this project is divided into four parts: [Backend](https://github.com/taranto/salesfy-backend), [Frontend](https://github.com/taranto/salesfy-frontend), [Shared](https://github.com/taranto/salesfy-shared) and [Test-Web](https://github.com/taranto/salesfy-test-web). Shared was our intermediate project which contained the business code and utilities that are used both by Backend and Frontend - as we did not want any duplicated logic. Besides that, Test-web belongs to e2e testing commands.  I (github.com/taranto) developed every single line of the Backend, Shared and most part of the Test-Web project. During this project period, we had two other developers besides me to work on the frontend section. The code is all here in github for you to see. 

### Project coding evolution and patterns

As I've dived into Typescript just after leaving Java, some old files may be a little javaish until more functional programming starts to go on. Some other routes started to get a cleaner code as I had time to build up a more consistent architecture. It had happened because primarily I needed to make my business live, only then I was able to do a non-verbose code.

Some verbose code are still there as they were already working bug-free and as I had all tests automated. At that time it was better to develop a new feature than spend time wiping up code. It would be better to wait until something was supposed to be done in those files to make a better code of it.

### Technologies

This project relies on a few technologies and programming languages. Those are:
- `Nodejs` - We knew we would be helped by the characteristics provided by the event loop from nodejs and an active community providing a broad source of libraries like in npm. The ability to program frontend and backend with a single language impacted this decision too.
- `Typescript` - The supertype is a resourceful layer that helps the programmers on productivity and consistency. No reason why not using this from the beginning.
- `React/React Native` - React is a robust and lightweight library which we could attach many libs from the community through npm. The ability of reusing the same language from the backend, and to be able to reuse components from web to mobile also impacted on this decision. 
- `AWS` - was the service chosen simply because we received credit for it on a few of our awards and that’s huge. Ec2, ses and s3 are not mandatory on how the system works, so it can be ported to gcloud services easily too.
- `Postgres` - We could be using mongo from the beginning, but the learning curve from all other technologies altogether was already a challenge. So the decision for this tech was straightaway by pure previous know-how.
- `Yarn` - We could be using npm to manage packages, but at that time it was only by taste.
- `Redis` - This technology was only used by micro memory usage portions of the backed to support a small and fast-paced storage
- `Selenium` - We wanted an established tool to help us on doing e2e tests and this was the one chosen. 
- `Linux` - choosing mac would impact our low budget. Choosing windows would make us need to make an extra effort to establish our local environment x servers. Why not use an OS we are already used to? That’s why our developers programmed on linux. The idea of using docker came way later on, in a phase we were already established and with lots of demands to take care of.

### Features

Some of the well-developed features of this project include:

- Login integrations with google and facebook;
- Sessions controlled by access and refresh tokens;
- Show metadata previews on links shared by users;
- Separated web and mobile deployed versions;
- Separation and links over folders/playbooks (technically called “channels”) and contents;
- Permission system for admins, users and guests;
- Usergroup system to link users and their respective channels;
- Responsive layout;
- Profile with avatar, password change, and password recovery through email;
- Push notifications;
- Star-rating system to evaluate contents quality;

### Final considerations

Maybe you may not start a Sales/Channel enablement business from this very project, but the built up architecture may fast forward any project as it has many things already implemented (and some routes samples there to be seen as a exemple). I hope you can make this project template the best of use :)




# Installation

### Installation requirements

The system may be compatible with newer versions of those technologies, but I can only guarantee the usage with the versions we were using back then.
* [postgres 9.6.11](https://www.postgresql.org/ftp/source/v9.6.11/)
* [nvm](https://www.freecodecamp.org/news/node-version-manager-nvm-install-guide/)
* [node 9.11.2](https://nodejs.org/download/release/v9.11.2/)
* [npm 5.6.0](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm)
* [yarn](https://www.hostinger.com/tutorials/how-to-install-yarn)
* [vscode](https://code.visualstudio.com/download) - recommended but not mandatory

### Installing [Shared](https://github.com/taranto/salesfy-shared) project

```sh
git clone https://github.com/taranto/salesfy-shared.git
yarn reinstall
yarn compile
yarn test
```

### Installing Database

In the folder you cloned the 'shared' project, clone backend project by it's side:

`git clone https://github.com/taranto/salesfy-backend.git`

Run in your database all code from the archieve `SQL changes.sql` and `SQL test env.sql`

### Installing [Backend](https://github.com/taranto/salesfy-backend) project

Into the salesfy-backend folder, duplicate the file `config.env.template` and rename it to `configTest.env`. Replace the unfilled keys.
`DB_` prefix are the ones for your database. `EMAIL_` prefix handles your email. `LOGIN_` and `S3_` are very specific, but not really necessary now. 

into the salesfy-backend folder, run:
```sh
$ yarn full-reinstall
$ yarn compile
$ yarn online
```

Add an user to the database quickly with the command: `yarn use-quick-register`

Shut down your online status, then:

`yarn test`

### Installing [Frontend](https://github.com/taranto/salesfy-frontend) project

In the folder you cloned shared project, clone frontend project by it's side:

`git clone https://github.com/taranto/salesfy-frontend.git`

*The app is not being able to install/work right now (only the web)

`yarn full-reinstall`

-Run the Backend project (`yarn online`)

`yarn web-dev`

### Installing [test-web](https://github.com/taranto/salesfy-test-web) project
In the folder you cloned shared project, clone test-web project by it's side:
`https://github.com/taranto/salesfy-test-web.git`
* Find your chrome version (usually at help -> about google chrome)
* Find your [chromedriver](https://sites.google.com/a/chromium.org/chromedriver/downloads) version compatible with your chrome.
*Actually the chromedriver's 2.38 version (the one commited) is associated to the version 65.0.3325.181 (official build) (64-bit) of chrome browser. It works well for the version 83.0.4103.39 of chrome browser (current version of 25/05/2020). If it doesn't work well, run `npm uninstall chromedriver` and `npm install chromedriver@xxx --save` switching `xxx` with the correct version.

`yarn full-reinstall`

`yarn compile`

* Switch the email/password of the test user according to your database (at src/Env.ts)
* Run the Backend project (`yarn online`)
* Run the Frontend project (`yarn web-dev`)
* Run this test project (`yarn test`)

*As soon as this project test runs, the chorme browser will open up by itself and a series of mouse clicks and keyboard types would start to be made automatically.
