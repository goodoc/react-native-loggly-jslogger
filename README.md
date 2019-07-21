React-native-loggly-jslogger
===============

Client-side React-native logger to use with Loggly gen2. Check out Loggly's [Javascript logging documentation](https://www.loggly.com/docs/javascript/) to learn more.
This is a fork of https://github.com/loggly/loggly-jslogger but working without browser constant.

Installation
------------
`npm install react-native-loggly-jslogger`
or
`yarn install react-native-loggly-jslogger`

Usage
-----
[this article from Loggly](https://www.loggly.com/blog/best-practices-for-client-side-logging-and-error-handling-in-react/) is a good starting point to instantiate your logger

```javascript
import { LogglyTracker } from 'react-native-loggly-jslogger';

const logger = new LogglyTracker();
// set your key
logger.push({ 'logglyKey': 'YOUR CUSTOMER TOKEN HERE' });

//push a string
logger.push('my tracking string');

//push a json;
logger.push({
  'text': 'my tracking string',
  'aList': [9, 2, 5],
  'anObject': {
    'id': 1,
    'value': 'foobar'
  }
})

```

Build min and map file
----------
You can build min and map file by using the command below:
```
npm install
grunt
```
