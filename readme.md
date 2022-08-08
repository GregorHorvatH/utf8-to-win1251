## Installation

Via [npm](https://www.npmjs.com/):

```bash
npm install utf8-to-win1251
```

Via [yarn](https://yarnpkg.com/):

```bash
yarn add utf8-to-win1251
```

In a browser or in [Node.js](https://nodejs.org/):

```js
import unicodeToWin1251 from 'utf8-to-win1251';
```

## API

This function takes a plain text string (the `input` parameter) and encodes it according to windows-1251. The return value is an environment-agnostic `Uint16Array` of which each element represents an octet as per windows-1251.

```js
import unicodeToWin1251 from 'utf8-to-win1251';
import saveAs from 'save-as';

const win1251Array = unicodeToWin1251('Доброго дня!');
const blob = new Blob([win1251Array], {
  type: 'text/plain;charset=windows-1251',
});

saveAs(blob, 'test-file.txt');
```

![text editor example of windows-1251 converted text](./example.png 'text editor example of windows-1251 converted text')
