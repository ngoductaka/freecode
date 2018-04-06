https://www.freecodecamp.org/challenges/drop-it
```javascript
function dropElements(arr, func) {
    var l = arr.length;
    for(var i=0; i<l; i++) {
        if(func(arr[0]))return arr;
        arr.shift();
    }
    return [];
}
dropElements([1, 2, 3, 7, 4], function(n) {return n > 3;});
```
