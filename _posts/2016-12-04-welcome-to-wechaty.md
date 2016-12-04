---
layout: post
title: Welcome to Wechaty!
date: '2016-12-04 14:04:27 +0800'
categories: news
published: true
---
Hello, world!

Today is a big day because Wechaty got a brand new Blog! ;-)

In the past half year, Wechaty growth from version 0.0.1 to 0.6.x. Today, it has dozens of pull requests, 100+ issues, 200+ stars, 1,400+ commits and 10,000+ lines of code.

### The Worlds Smallest ChatBot

Wechaty is a easy to use **ChatBot Framework** which can help you write **the worlds smallest chatbot**. Maybe you are very interesting in ChatBot industory, or you just want to get your own wechat personal account robot, Wechaty will always be your friend.

The following 6 lines javascript code example will show you how does Wechaty work:

```javascript
const { Wechaty } = require('wechaty')

Wechaty.instance() // Singleton
.on('scan', (url, code) => console.log(`Scan QR Code to login: ${code}\n${url}`))
.on('login',       user => console.log(`User ${user} logined`))
.on('message',  message => console.log(`Message: ${message}`))
.init()
```

How to run this piece of code? Easy. Wechaty has a docker image which can help you put your bot on duty in seconds:

```shell
$ docker run -ti --rm --volume="$(pwd)":/bot zixia/wechaty mybot.js
```

> Source code is saved to file: `mybot.js`

See? death easy to use!

### Last but not least

* Check out the [Wechaty IO][wechaty-io] for more info on how to get the most out of Wechaty. 
* File all bugs/feature requests at [Wechaty’s GitHub repo][wechaty-gh]. 
* If you have questions, you can ask other developers in _Wechaty Developers' Home_ by scan belowing Qr Code and send the secret code: `wechaty`.

![Wechaty Developers' Home][wechaty-qrcode-image]

_secret code: `wechaty`_


Cheers! 

Best,

Huan, a ChatBot & Deep Learning Fan

[wechaty-gh]: https://github.com/wechaty/wechaty/
[wechaty-io]: https://www.wechaty.io/
[wechaty-qrcode-image]: https://raw.githubusercontent.com/wechaty/wechaty/master/image/BotQrcode.png
