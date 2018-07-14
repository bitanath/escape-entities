# Escape HTML entities like `&#9830;` or `&diams;` to 💎

Use in either nodejs or the browser. It's really simple and works pretty fast. 

## Installation
Browser 🌎 : [https://cdn.jsdelivr.net/npm/entity-escape@latest/index.min.js](https://cdn.jsdelivr.net/npm/entity-escape@latest/index.min.js)

Node.js 🛠 : `npm install --save entity-escape`

## Usage

Browser:

```js
var text1 = Entities.unescape('The big &amp; and sparkly diamond &#40; almost &#41; glittered in the dark.');

var text2 = Entities.escape('This is a diamond ♦, watch it ◊');

console.log(text1,text2);

```

Node.js:

```js
const Entities = require('entity-escape');

var text1 = Entities.unescape('The big &amp; and sparkly diamond &#40; almost &#41; glittered in the dark.');

var text2 = Entities.escape('This is a diamond ♦, watch it ◊');

console.log(text1,text2);

```

## Methods and Options

```js
Entities.unescape(text,options); //options are {silent:false(default on node, true default on browser),replaceNumbers:true(true default on node, replaces numbered entities even if no names are present)}

Entities.escape(text,options); //options are {silent:false(default on node, true default on browser)}
```

In case `{silent:true}` no output is rendered to the console. In case `replaceNumbers:false` only those characters which are explicitly named HTML entities will be replaced.