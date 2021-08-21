# JavaScript_Coding
---
## Day1
---
### Second Largest Element in an array

```javascript
function secondLargest(nums){
   largest=nums[0];
   secondlargest=nums[0];

   for(let i=1;i<nums.length;i++){
       if(nums[i]>largest){
           secondlargest=largest;
           largest=nums[i];
           continue;
       }
       if(nums[i]<largest && nums[i]>secondlargest){
           secondlargest=nums[i];
       }
   }
   return secondlargest;
}

console.log(secondLargest([2,3,4,6,6,5]))
```
### Create a function and It has two parameters: a and b . It must return an object modeling a rectangle that has the following properties: length , width, parameter,and area

``` javascript
function Rectangle(a, b) {
    let obj={
        length: a,
        width: b,
        perimeter: 2*(a+b),
        area: a*b
    }
    return obj;   
}

console.table(Rectangle(4,5))
```
### Complete the function in the editor. It has one parameter: an array,a , of objects. Each object in the array has two integer properties denoted by x and y. The function must return a count of all such objects o in array a that satisfy . o.x===o.y

``` javascript

function getCount(objects) {
    let count=0;
    for(let i=0;i<objects.length;i++){
        if(objects[i].x===objects[i].y){
            count++;
        }
    }
    return count;
}
let obj=[
    {
        x:1,
        y:1
    },
    {
        x:2,
        y:3
    },
    {
        x:3,
        y:3
    },
    {
        x:4,
        y:5
    },{
        x:3,
        y:6
    }
]
console.log(getCount(obj))
```

### Try, Catch and Finally

``` javascript

function reverseString(s) {
    try{
        console.log(s.split('').reverse().join(''))
    }catch(err){
        console.log(err.message)
    }finally{
        console.log(s)
    }
}

reverseString('1234')
reverseString(1234)
```

### Create a Polygon class that has the following properties:

- A constructor that takes an array of integer values describing the lengths of the polygon's sides.
- A perimeter() method that returns the polygon's perimeter.

``` javascript
class Polygon{
    constructor(arr){
        this.arr=arr;
    }
    perimeter(){
        let sum=0;
        for(let i=0;i<this.arr.length;i++){
            sum+=this.arr[i];
        }
        return sum;
    }
}
let triangle=new Polygon([1,2,3,4])
console.log(triangle.perimeter())
```

``` javascript
class Polygon{
    constructor(arr){
        this.arr=arr;
    }
    perimeter(){
        return this.arr.reduce((a,b)=>{
            return a+b;
        },0)
    }
}

let triangle=new Polygon([3,4,1,9,3])
console.log(triangle.perimeter())
```

### Write the function. It has one parameter: an array,nums . It must iterate through the array performing one of the following actions on each element:

- If the element is even, multiply the element by 2.
- If the element is odd, multiply the element by 3.

``` javascript
function modifyArray(nums) {
    return nums.map(item=> item%2===0? item*2: item*3)
}

console.log(modifyArray([1,3,2,4,8,9,0,5]))
```
---
## Day2
### We define S to be a sequence of distinct sequential integers from 1 to n ; in other words,S={1,2,3,...n} .We want to know the maximum bitwise AND value of any two integers,  a and b (where a<b ), in sequence S that is also less than a given integer, k.Complete the function in the editor so that given n and k, it returns the maximum a&b <k.

``` javascript
function getMaxLessThanK(n,k){
    let max_value=0;
    
    for(let i=1;i<n;i++){
        for(let j=i+1;j<n+1;j++){
            if(Number(i & j)<k){
                if(Number(i & j)>max_value){
                    max_value=i&j;
                }
            }
        }
    }
    return max_value;
}

console.log(getMaxLessThanK(5,2))
```
