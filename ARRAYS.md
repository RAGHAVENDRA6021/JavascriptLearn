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
- splice(startIndex,delteCount,elementsToADD) - can insert in between and delete elements contiguously in the same array, negative indexes are allowed
- slice(startIndex,LastIndex) - get ranges of the array and returns new array, so created new copy
### Adding arrays to concat
```js
const a= [1,2,3]
const b= [2,4,6].concat(a) // returns new array 
```

### indexOf , lastIndexOf()
* indexOf() returns first index of element if present , else -1
* lastIndexOf() - returns last index , else -1
```js
const a=[1,2,2,3,2]
console.log(a.indexOf(a))//1
console.log(a.lastIndexOf(a))//4
```
here drawback is , we can find index if array element is object and trying to find index
### find() and findIndex()
```js
const users=[{'name':'raghava'},{'name':'rebel'}]
const rebel=users.find((ele,index,data)=>ele.name==='rebel') // returns that object
const rebelIndex = users.findIndex((ele,index,data)=>ele.name==='rebel')
```
### inclusion
```js
[1,22,3].includes(22)//true if present, else false
```

### loops

#### forEach() loop
```js
const prices = [10.99,5,2,4.3]
const tax=0.19
const newPrices=[] 
prices.forEach((ele,index)=>newPrices.push(ele*tax))
```

#### map() -returns new array of same size
```js
const prices = [10.99,5,2,4.3]
const tax=0.1
const newPrices=prices.map((ele,index)=>ele*tax) // [1.099,0.5,0.2,0.43]
```
#### sort()

```js
const prices =[1,4,23,5,8]
prices.sort((a,b)=>{
   if(a>b) return 1;
   else if(a==b) return 0;
   else return -1;
})
```

#### reverse()

#### filter() -filters array
```js
const prices =[1,4,23,5,8]
const filteredArray = prices.filter((ele)=>ele>5)//[1.23,8]
```

#### reduce() 
```js
const prices =[1,4,23,5,8]
//find sum of all prices
const sum = prices.reduce((acc,val,index)=>{
   return acc+val
},0)
const multiply = prices.reduce((acc,val,index)=>{
   return acc*val
},1)
```
#### split() - splits strings into an array  with given seperator
#### join() - join array into string with given seperator
```js
const s='i am raghava'.split(' ')//['i','am','raghava']
const j= ['i','am','raghava'].joing('$')//'i$am$raghava'
```

#### spread operator -copies into new array
```js
const a=[1,2,3]
const b=[...a] //copies new array
a.push(4)
console.log(a)//[1,2,3,4]
console.log(b)//[1,2,3]
const users=[{'name':'raghava'},{'name':'rebel'}]
const copiedUsers=[...users]
users[1].name='john'
console.log(copiedUsers)//[{'name':'raghava'},{'name':'john'}]
// it copies new element , for objects same reference are passed
//to solve
const new = [...users.map((user)=>({name:user.name}))]
```

#### array destructuring
```js
const nameData=['raghava','rebel']
const [firstName,lastName]=nameData
```
