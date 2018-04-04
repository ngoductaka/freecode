# Diff Two Arrays 
## `cách 1`
```javascript
function diffArray(...arr) {
  const newArr = [];
  for(let i=0,{length}=arr;i<length;i++) newArr.push(...arr[i]);
  const obj={};
  newArr.forEach(e=>{
    if(obj[e]===undefined) obj[e]=0;
    obj[e]++;
  });
  const result =[];
  for(let e in obj) if(obj[e]===1)result.push(!+e?e:+e);
  return result;
}
diffArray(["diorite", "andesite", "grass", "dirt", "pink wool", "dead shrub"], ["diorite", "andesite", "grass", "dirt", "dead shrub"]);
```
## `cách 2`
```javascript
function diffArray(...arr) {
  return [...arr[0].filter(e=>{
    if(arr[1].indexOf(e)===-1) return e;
  }),...arr[1].filter(e=>{
    if(arr[0].indexOf(e)===-1) return e;
  })];
}
diffArray(["diorite", "andesite", "grass", "dirt", "pink wool", "dead shrub"], ["diorite", "andesite", "grass", "dirt", "dead shrub"]);
```
## cách 3
```javascript
function diffArray(...arr) {
  return [...arr[0].filter(e=>arr[1].indexOf(e)===-1),...arr[1].filter(e=>arr[0].indexOf(e)===-1)];
}
diffArray(["diorite", "andesite", "grass", "dirt", "pink wool", "dead shrub"], ["diorite", "andesite", "grass", "dirt", "dead shrub"]);
```
# Sum All Numbers in a Range 
```javascript
function sumAll(arr) {
  const max = Math.max(...arr), min = Math.min(...arr),result = [];
  for(let i = min; i<=max; i++)  result.push(i);
  return result.reduce((a, b) => a + b);
}
sumAll([1, 4]);
```
