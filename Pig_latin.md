# Pig Latin

link: https://www.freecodecamp.org/challenges/pig-latin

```javasrcipt

function translatePigLatin(str) {
    const arr = str.split('');
    const {length} = arr;
    for(let i = 0; i < length; i++) {
      if( ['u','e','a','o','i'].includes(arr[i]) ) {
        var k = i; break;
      }
    }
    if (k===0) return str+"way";
    arr.splice(0, k);
    return ([...arr,str.substr(0,k),'ay'].join(""));
}
translatePigLatin("consonant");

```
`cach 2`
```javascript
function translatePigLatin(str) {
    const arr = str.split('');
    const {length} = arr;
    const k = str.search(/[aeiou]/);
    if (k===0) return str+"way";
    arr.splice(0, k);
    return ([...arr,str.substr(0,k),'ay'].join(""));
}
```
`cach 3`
```javascript
function translatePigLatin(str) {
    if (str.search(/[aeiou]/)===0) return str+"way";
    return str.replace(/([^ueoai]+)([ueoai].*)/i, `$2$1ay`);
}
```
