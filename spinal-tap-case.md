link: https://www.freecodecamp.org/challenges/spinal-tap-case
```javascript
const spinalCase = str => str.replace(/([a-z])([A-Z])|[\W\d_]+/g, `$1-$2`).toLowerCase();
spinalCase('AllThe-small-+*/056 _Things');
```
