# link : https://www.freecodecamp.org/challenges/no-repeats-please
## bài toán: 
cho 1 chuỗi các ký tự.<br>
trã về tổng số các hoán vị từ dãy.<br>
điều kiện: 2 chữ cái g nhau thì không đứng cạnh nhau<br>
ví dụ: `aab` có các hoán vị `aab, aab, aba, aba, baa, baa` chỉ có `aba, aba ` là thỏa mãn điều kiện 
## solution:
```javascript
function permAlone(str) {
  // 
  const arr = str.split('');
  const {length} = arr;
  // kết quả
  const result = [];
  // hàm kiểm tra giá trị 
  const check=(val, next) => val[val.length-1] !== next;
  // hàm quay lui
  const Try = (val,next) => {
    for(let i = 0; i<next.length; i++){
      //check giá trị tiếp và trị cuối mảng 
      if(check(val,next[i])){
        // thỏa mãn chèn vào cuối
        let valNext = val.concat(next[i]);
        let [..._next] = arr;
        valNext.forEach(e=> _next.splice(_next.indexOf(e),1) );
        // nếu đủ độ dài 
        if(valNext.length === length)  result.push(valNext);
        // nếu không tiếp tục thử 
        else  Try(valNext ,_next);
      } 
    }
  };
  
  Try([],arr);
  result.map(e=>console.log(e));
  console.log(result.length);
  return result.length;
}
permAlone('aabc');
```
