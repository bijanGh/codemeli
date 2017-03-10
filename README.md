# codemeli
National number validator for Iranians.

**Node.js**

Get package from npm :
```bash
npm install --save codemeli
# or using yarn
yarn add codemeli
```

**Browser**

Add this tag:
```html
    <script src="https://unpkg.com/codemeli/lib/codemeli.js"></script> 
```

## API
This packages exports `codemeli(code,returnObj)` function: (`xxxxxxxxxx` is just for demo only)

**code**
Input national number value. it can be string or number, both are supported.

**[return value]**
If for any reason input is invalid it will return `null` Otherwise It will return a formatted **10 digits** code.

If returnObj is true (defaults to `false`) function will return an object with this fields instead:
- code
- parity
- city_code
- uid

## Example

```js
const codemeli = require('codemeli');

var inputValue='xxxxxxxxxx'; // TODO: Change this value

// Simple usage
const national_number = codemeli(inputValue);
console.log(national_number); // xxxxxxxxxx

// Object style
const national_number_obj = codemeli(inputValue, true);
console.log(national_number_obj);
/*
{ code: 'xxxxxxxxxx',
  parity: 'x',
  city_code: 'xx',
  uid: 'xxxxxxx' }
*/
``` 

# LICENSE
MIT License Copyright (c) 2017 Fandogh - Pooya Parsa <pooya@pi0.ir>.   
Validation algorithm extracted from an article from [aliarash.com](http://www.aliarash.com/article/codemeli/codemeli.htm)
So original credits backs to [Ali Arash](mailto:admin@aliarash.com)