## baidu-voice
文字转语音百度API简单封装

## 下载安装

```
$ git clone https://github.com/dreamans/baidu-voice.git
$ cd baidu-voice/src
$ npm install
```

修改 src/config.js 中配置文件

```
    app_id: '', // 百度API appid 

    app_key:  '', // 百度API appkey 

    secret_key: '', //百度API Secret key

    port: 8068 // http服务端口
```

## 运行

```
$ npm run web
```

输入网址

http://127.0.0.1:8068/?speech=你好&per=1&spd=1&pit=1&vol=1

参数说明:
* speech - 要转成语音的文字
* per - 发音人选择, 0为女声，1为男声，3为情感合成-度逍遥，4为情感合成-度丫丫，默认为普通女
* spd - 语速，取值0-9， 默认为5中语速
* pit - 音调，取值0-9， 默认为5中语调
* vol - 音量，取值0-15，默认为5中音量

请求返回的数据类型为 `audio/mpeg` 在浏览器中即可收听

若有报错，可在 src/nohup.out 中查看

