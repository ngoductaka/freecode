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
