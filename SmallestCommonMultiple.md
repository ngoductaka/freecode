# Smallest Common Multiple (https://www.freecodecamp.org/challenges/smallest-common-multiple)
```javascript
function bcnn(a,b) {
    if(a==b) return a;
    var max = Math.max(a,b), min = Math.min(a,b), n= parseInt(max/min) +1;
    if(max%min===0) return max;
    for(var i=n; i<=max; i++){
        if((i*min)%max==0){
            return i*min;
        }
    }
}

function smallestCommons(arr) {
    var max=Math.max(arr[0],arr[1]), min = Math.min(arr[0],arr[1]), arr =[];
    for(let i = min; i<= max; i++) arr.push(i);
    return arr.reduce((c,n)=>bcnn(c,n));
}
  
smallestCommons([6,5]);
  
```
` cach 2`
```javascript
function bcnn(a,b) {
    if(a==b) return a;
    var max = Math.max(a,b), min = Math.min(a,b), n= parseInt(max/min) +1;
    if(max%min===0) return max;
    for(var i=n; i<=max; i++){
        if((i*min)%max==0){
            return i*min;
        }
    }
}

function smallestCommons(arr) {
    var max=Math.max(arr[0],arr[1]), min = Math.min(arr[0],arr[1]),result=1;
    for(var i=min; i<= max; i++){
        result=bcnn(i,result);
        console.log(result);
    }
    return result;
}
  
  
  smallestCommons([6,5]);
  
```
