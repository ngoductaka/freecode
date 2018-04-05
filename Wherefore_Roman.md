# Wherefore art thou
* link :https://www.freecodecamp.org/challenges/wherefore-art-thou
```javascript
function whatIsInAName(collection, source) {
  var arr = [];
  collection.forEach(e => {
    if((Object.keys(source)).every(k=> e[k]===source[k]) ) arr.push(e);
  });
  return arr;
}
```
` cach 2 `
```javascript
const whatIsInAName=(collection, source)=> return collection.filter(e => (Object.keys(source)).every(k=> e[k]===source[k]) )

```
# Roman Numeral Converter
* link: https://www.freecodecamp.org/challenges/roman-numeral-converter
```javascript
'use strict';

function convertToRoman(n) {
    var ro = {
      '1': 'I',
      '5': 'V',
      '10': 'X',
      '50': 'L',
      '100': 'C',
      '500': 'D',
      '1000': 'M'
  };

  var numToArr = function numToArr(n) {
      var str = n.toString(),
          m = str.length - 1,
          re = [];
      for (var i = 0; i <= m; i++) {
          re.push(+str[i] * Math.pow(10, m - i));
      }return re;
  };

  var add = function add(num) {
      var x = ('' + num).length - 1;
      var y = Math.pow(10, x);
      // console.log(y);
      var o = '' + y;
      var f = '' + 5 * y;
      var t = '' + 10 * y;
      var dnd = [ro[o], ro[o] + ro[o], ro[o] + ro[o] + ro[o], ro[o] + ro[f], ro[f], ro[f] + ro[o], ro[f] + ro[o] + ro[o], ro[f] + ro[o] + ro[o] + ro[o], ro[o] + ro[t]];
      return dnd[num / y - 1];
      // console.log(num/y);
  };
  var resu = [];
    var arr = numToArr(n);
    arr.map(function (e) {
        resu=resu.concat(add(e));
    });
    //     console.log(resu.join(''));
//   var ddd = resu
    return resu.join("");
}
// convert(1995);
convertToRoman(12);
// convertToRoman(36);
```
