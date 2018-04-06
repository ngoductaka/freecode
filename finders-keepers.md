(https://www.freecodecamp.org/challenges/finders-keepers)
```javascript
function findElement(arr, func) {
    for(var j=0; j<arr.length; j++) if(func(arr[j])) return arr[j]; 
    }  
  
findElement([1, 2, 3, 4], function(num){ return num % 2 === 0; });
```
