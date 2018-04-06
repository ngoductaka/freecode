# Search and Replace:
link: https://www.freecodecamp.org/challenges/search-and-replace
```javascript
function myReplace(str, before, after) {
  let reg = new RegExp(before,'i');
  if(before.charAt(0).toUpperCase()===before.charAt(0)) return str.replace(reg,after.charAt(0).toUpperCase() + after.slice(1));
  return str.replace(reg,after);
}

myReplace("This has a spellngi error", "spellngi", "spelling");
```
