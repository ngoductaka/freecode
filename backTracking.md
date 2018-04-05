# bài toán xếp hậu
```javascript
//size of chessboard
const n = 3;
//array store result 
const hau = [];
// set value default 
for (let i = 0; i <= n; i++) hau[i] = -1
// check next value in array result  
const check = (i,j) => {
    // first row
    if (i===0) return true;
    for (let index = 0; index < i; index++) {
        // have same colum
        if (hau[index]===j) return false;
        // diagonal line 
        if (Math.abs(index-i)===Math.abs(hau[index]-j)) return false;
    }
    return true;
}
// check result array is complete 
const ok =(arr) => arr.every(e=>e!==-1)
// prinf result 
const expor = arr => console.log(arr)
// function backtracking
const Try = (i) => {
    for(let j = 0; j <= 3; j++) {
        if (check(i,j)&&hau[i]===-1) {
            hau[i] = j;
            let next = i+1;
            if (ok(hau)) expor(hau)  
            else  Try(next)
            hau[i] = -1;
        }
    }
}

Try(0);
```
