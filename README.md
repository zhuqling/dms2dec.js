dms2dec.js
==========

Degrees, minutes, seconds (sexagesimal) to decimal GPS positions. Useful for
parsing PGS exif tags in geotagged images.

## Install

### Node/npm

```bash
npm install dms2dec --save
```

```javascript
dms2dec = require('dms2dec');
```

### Web

```html
<script language="JavaScript" src="/dms2dec.js"></script>
```

## Usage

[`latDec`, `lonDec`] = dns2dec(String `lat`, String `latRef`, String `lon`, String `lonRef`);

### Parse dms strings

```javascript
var dec = dms2dec("60/1, 21/1, 4045/100", "N", "5/1, 22/1, 1555/100", "E");
// dec[0] == 60.36123611111111, dec[1] == 5.370986111111111
```

### Parse dms arrays

```javascript
var dec = dms2dec(["60/1", "21/1", "4045/100"], "N", ["5/1", "22/1", "1555/100"], "E");
// dec[0] == 60.36123611111111, dec[1] == 5.370986111111111
```

#### dms arrays as decimal

```javascript
var dec = dms2dec([60, 21, 40.45], "N", [5, 22, 15.55], "E");
// dec[0] == 60.36123611111111, dec[1] == 5.370986111111111
```
