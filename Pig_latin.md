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
