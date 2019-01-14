# king-bot-api <!-- omit in toc -->

this is a really high performance based bot for [travian kingdoms](https://www.kingdoms.com/) written in typescript.  
it's designed to run in a console for better server support.

feel free to join the [official discord channel](https://discord.gg/5n2btF7) or **[contact me! (:](mailto:f.breuer@scriptworld.net)**

i made a video tutorial on how to setup the bot with it's features ! **[click me !](https://youtu.be/h6XJ56CT6XQ)**

you want to run the bot **24/7**, but don't want to use your computer? **[contact me aswell! (:](mailto:f.breuer@scriptworld.net)**

[![ko-fi](https://img.shields.io/badge/buy%20me%20a-coffee-yellowgreen.svg)](https://ko-fi.com/Y8Y6KZHJ)
[![Build Status](https://travis-ci.org/scriptworld-git/king-bot-api.svg?branch=master)](https://travis-ci.org/scriptworld-git/king-bot-api)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/1143396b01b944b28252861dc3762d7a)](https://www.codacy.com/app/scriptworld-git/king-bot-api?utm_source=github.com&utm_medium=referral&utm_content=scriptworld-git/king-bot-api&utm_campaign=Badge_Grade)
[![MIT license](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/scriptworld-git/king-bot/blob/master/LICENSE)

# table of contents <!-- omit in toc -->

- [getting-started](#getting-started)
- [gui](#gui)
  - [features](#features)
  - [screenshots](#screenshots)
- [docker](#docker)
- [development](#development)
- [thank you for](#thank-you-for)

# getting-started

[use docker](#docker)

**or**

1. install latest version of [nodeJS](https://nodejs.org/)
2. clone or download this repository
3. open project in console
4. install all dependencies
    1. `$ npm install`
5. build the project
    1. `$ npm run build`
6. edit `main.js`
    1. look up `sample_main.js` for help
7. start the bot
    1. `$ npm start`

after changing `main.js` only use `$ npm start` to restart the bot.  
when downloading a new project version you have to `$ npm install && npm run build` again before starting the bot.

# gui

1.  provide your login credentials in `main.js`.
1.  `$ npm start`
1.  open `http://localhost:3000/` in your browser and explore the bot

after configuring you can close the browser window and the bot keeps running until you exit it in the console (CTRL + C).

## features

-   send farmlist in interval
-   endless building queue
-	auto raise fields
-   auto adventure
-   finish 5 min earlier
-   inactive finder
-   easy scout
-   custom trade routes

## screenshots

![interface](https://scriptworld.net/assets/king-bot-api/home.png)  
![farming](https://scriptworld.net/assets/king-bot-api/farmlist.png)

# docker

there is also a docker image for this bot.  
create a folder for the database and a file (`cred.txt`) with your credentials in this folder that can be mounted to the docker container:

```csv
your_email;your_password;your_gameworld
```

pull image and start the container mounting the file:

```console
$ docker pull scriptworld/king-bot-api
$ sudo bash ./docker.sh
```
the docker script will prompt you for a container name, what port you want the bot to run on and the absoulute path to the folder you just created.

visit `http://localhost:3000` (or whatever port you chose) to see the results.

# development

if you wanna use the command `npm run dev` or `npm run watch` you need to insert your credentials into `dev_main.js`.  
you can also create a file names `cred.txt` in the root folder which contains your login credentials:

```csv
your_email@mail.com;your_password;your_gameworld
```

this file will be ignored by git so you don't have to be scared to accidentally commit your credentials.

create a file names `own_main.js` which is going to be ignore by git, you can modify it as you wish, without pushing your custom feature set to github.

# thank you for

beeing active since the first day of this project **[@didadadida93](https://github.com/didadadida93)**  
keeping the issue page alive **[@OneManDevz](https://github.com/OneManDevz)**  
programming auto adventure **[@Tom-Boyd](https://github.com/Tom-Boyd)**  
programming trade routes **[@tmfoltz](https://github.com/tmfoltz)**  

---

_we love lowercase_
