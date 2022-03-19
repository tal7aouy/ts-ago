# ts-ago

a simple library used to format datetime with `*** time ago` statement into readable format. eg: '3 hours ago'

Formats a timestamp to:

- just now
- 3 minutes ago
- 5 hours ago
- 8 days ago
- 6 months ago
- 4 years ago

## Install

Get it on [npm](https://www.npmjs.com/package/ts-ago)

```bash
npm install ts-ago
```

Get it on [yarn](https://yarnpkg.com/package/ts-ago)

```bash
yarn add  ts-ago
```

## Usage

This module exports a main function 'ago()' that takes one argument 'timestamp' and returns
timestamp formated in a readable form:

```js
import ago from "ts-ago";

// Timestamps for one minute, one hour, one day, one month and one year
const minute = 60 * 1000;
const hour = 60 * minute;
const day = 24 * hour;
const month = 30 * day;
const year = 12 * month;

// simulating different inputs
const nowTimestamp = new Date().getTime(); // now
const fiveMinutesAgoTimestamp = nowTimestamp - 5 * minute; // timestamp for 5 minutes ago
const fiveHoursAgoTimestamp = nowTimestamp - 5 * hour; // timestamp for 5 hours ago
const fiveDaysAgoTimestamp = nowTimestamp - 5 * day; // timestamp for 5 days ago
const fiveMonthsAgoTimestamp = nowTimestamp - 5 * month; // timestamp for 5 months ago
const fiveYearsAgoTimestamp = nowTimestamp - 5 * year; // timestamp for 5 years ago

// using ago()
ago(); // returns undefined
ago("hello world"); // throws an Error
ago(nowTimestamp); // returns 'just now'
ago(fiveMinutesAgoTimestamp); // returns '5 minutes ago'
ago(fiveHoursAgoTimestamp); // returns '5 hours ago'
ago(fiveDaysAgoTimestamp); // returns '5 days ago'
ago(fiveMonthsAgoTimestamp); // returns '5 months ago'
ago(fiveYearsAgoTimestamp); // returns '5 years ago'
```

## License

[MIT License](LICENSE)
