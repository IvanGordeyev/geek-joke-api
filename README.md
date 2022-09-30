# Geek-Jokes

## A RESTful API to get random geek jokes written in Flask
[![forthebadge](http://forthebadge.com/images/badges/made-with-python.svg)](http://forthebadge.com)
[![forthebadge](http://forthebadge.com/images/badges/gluten-free.svg)](http://forthebadge.com)

## What is the Geek-Jokes-api?
The Geek Jokes RESTful API lets you fetch a random geeky/programming related joke for use in all sorts of applications.

## Why the Geek-Jokes-api?
The Geek Jokes api is for any developer needing some random (geeky) jokes in their life or application.

## URL
```
GET: https://geek-jokes.sameerkumar.website/api?format=json
```

## Usage
Just do a GET request on the API URL.
```
GET: https://geek-jokes.sameerkumar.website/api?format=json
```

## Projects using Geek Jokes API

Repository | Description
---- | ----
[Random. Django. Rango.](https://github.com/powerhouseofthecell/rango) | Random. Django. Rango. An introduction to using Python and Django to build a website.
[tellmejoke](https://github.com/MunafHajir/-tellmeajoke) | VS Code Extension that tells you a joke

Used Geek Jokes API in your project? Check out the [contributing guidelines](https://github.com/sameerkumar18/geek-joke-api/blob/master/contributing.md) for this list and let us know. we love PRs :)

## Examples

### cURL
```
curl -X GET \
'https://geek-jokes.sameerkumar.website/api?format=json'
```

### Python
```Python
import requests

requests.get('https://geek-jokes.sameerkumar.website/api?format=json')
```

### Node.js (es6)
```Javascript
var request = require('request');

let options = {
    url: 'https://geek-jokes.sameerkumar.website/api?format=json',
    method: 'GET'
}

request(options, (err, response, body) => {
    if(!err && response.statusCode == 200)
        console.log(body)
});
```

 ### Any browser
 visit the url: https://geek-jokes.sameerkumar.website/api?format=json to get a joke. Press refresh button for more jokes.

 ### Node-Red (output to Google Home speaker on repeat)
![Screenshot from 2022-09-30 19-21-12](https://user-images.githubusercontent.com/48790568/193333026-3a610c38-a5db-4425-a56c-40fb26f4a727.png)
```Node-Red
[
    {
        "id": "46bb755fadefbd98",
        "type": "tab",
        "label": "Jokes API",
        "disabled": false,
        "info": "",
        "env": []
    },
    {
        "id": "7bdcd3db4604f441",
        "type": "inject",
        "z": "46bb755fadefbd98",
        "name": "",
        "props": [
            {
                "p": "payload"
            },
            {
                "p": "topic",
                "vt": "str"
            }
        ],
        "repeat": "60",
        "crontab": "",
        "once": true,
        "onceDelay": "10",
        "topic": "",
        "payloadType": "date",
        "x": 180,
        "y": 220,
        "wires": [
            [
                "450f3c09549e7b0f"
            ]
        ]
    },
    {
        "id": "450f3c09549e7b0f",
        "type": "http request",
        "z": "46bb755fadefbd98",
        "name": "",
        "method": "GET",
        "ret": "txt",
        "paytoqs": "ignore",
        "url": "https://geek-jokes.sameerkumar.website/api",
        "tls": "",
        "persist": false,
        "proxy": "",
        "authType": "",
        "senderr": false,
        "x": 240,
        "y": 480,
        "wires": [
            [
                "c07e6025014c5b6f"
            ]
        ]
    },
    {
        "id": "c07e6025014c5b6f",
        "type": "cast-to-client",
        "z": "46bb755fadefbd98",
        "name": "Message from Input",
        "url": "",
        "contentType": "",
        "message": "",
        "language": "en",
        "ip": "192.168.0.13",
        "port": "8009",
        "volume": "30",
        "x": 600,
        "y": 480,
        "wires": [
            []
        ]
    }
]

```

## License
MIT

## Contact
Contact: [sam@sameerkumar.website](mailto:sam@sameerkumar.website)

## Author
Sameer Kumar
https://sameerkumar.website
