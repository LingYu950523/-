## （1）
setTimeout() 是属于 window 的方法，该方法用于在指定的毫秒数后调用函数或计算表达式。
即该方法在等待后执行函数，意思就是尽快，而不是马上。

```javascript
let i = 0
for(i = 0; i<6; i++){
  setTimeout(()=>{
    console.log(i)
  },0)
}
```
上述代码中，setTimeout中的定时器并不是准确的时间，实际中它需要在执行完前面的函数后才定时执行。
因此先执行完循环，再打印出参数，此时参数已经发生了变化。

## （2）
```javascript
for(let i = 0; i<6; i++){
  setTimeout(()=>{
    console.log(i)
  },0)
}
```

## (3)
```javascript
for(i = 0; i<6; i++){
  !function(j){
      setTimeout(()=>{
        console.log(j)
      },0)
  }(i)
}
```
利用立即执行函数。
