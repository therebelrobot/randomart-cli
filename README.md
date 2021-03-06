randomart-generator
====

Generate OpenSSH style "randomart" images based on any data.

This is a shameless, cli port of [slapresta/randomart](https://github.com/slapresta/randomart), which is itself a shameless, slightly modified port of [calmh/randomart](https://github.com/calmh/randomart) to JS.

Example
====

```javascript

randomart = require('randomart');

console.log(randomart([
  0x9b, 0x4c, 0x7b, 0xce, 0x7a, 0xbd, 0x0a, 0x13,
  0x61, 0xfb, 0x17, 0xc2, 0x06, 0x12, 0x0c, 0xed
]));
```

```
    .+.
      o.
     .. +
      Eo =
        S + .
       o B . .
        B o..
         *...
        .o+...
```

Documentation
====

The function returned by `require('randomart')` optionally accepts two arguments: the first one, `data`, is expected to be an array of integers between 0 and 255, while the second one, `options`, has the following structure, in which all parent elements are optional:

```json
{
  "bounds": {
    "width": 17,
    "height": 9,
  },
  "symbols": {
    "-2": "E",
    "-1": "S",
     "0": " ",
     "1": ".",
    [...]
    "13": "/",
    "14": "^"
  }
}
```

Credits
====

Thanks to [@calmh](https://github.com/calmh) for their hard work! May the opensource gods reward them with seventy-two non-terrible window managers.
