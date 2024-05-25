![Node.js Package](https://github.com/hishprorg/atque-at/workflows/Node.js%20Package/badge.svg?branch=master)  

@hishprorg/atque-at
=================

Download images from remote URLs or use local images and encode/decode them to Base64 string or [Buffer](https://nodejs.org/api/buffer.html) object

### Installation  
`npm i @hishprorg/atque-at --save`  

### Usage  
```js
const base64 = require('@hishprorg/atque-at');
// or
import {encode, decode} from '@hishprorg/atque-at';
```   

### Examples
```js
// encoding a jpg to base64
const url = 'https://example.com/test.jpg';
const options = {
  string: true,
  headers: {
    "User-Agent": "my-app"
  }
};

// writing to file named 'example.jpg'
const image = await encode(url, options);
await decode(image, { fname: 'example', ext: 'jpg' });

// writing to a sub-directory
// after creating a directory called 'photos'
const image = await encode(url, options);
await decode(image, { fname: './photos/example', ext: 'jpg' });
```  

### Contributing
Read the [CONTRIBUTING](CONTRIBUTING.md) guide for information.  

### License  
Licensed under MIT. See [LICENSE](LICENSE) for more information.  

### Issues  
Report a bug in issues.   

Made with love in Dhaka, Bangladesh by [Riyadh Al Nur](https://verticalaxisbd.com)
