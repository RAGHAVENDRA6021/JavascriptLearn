# Arrays

## creating arrays

1. const ele=[1,2,3,4,5]
2. using new keyword
   - cont ele =new Array(2,3,4)//[2,3,4]
   - const ele= new Arrays(5) //creates an array of size 5
3. of keyword
   - const ele= Array.of('hi') //['hi']
4. from keyword
   - const ele = Array.from([1,2,3]) // it converts array like objects , iterables to real array

```js
const ele = document.querySelectorAll();
const arr = Array.from(ele);

//now changing ele values will have effect in ui
// but in arr, there wont be any effect
```

### looping over arrays

```js
for (let ele of arr) {
  console.log(ele);
}
```

### methods in arrays

- push() - adding element at end
- unshift() - adding element at first
- pop() - remove element at end
- shift() - remove element at first
