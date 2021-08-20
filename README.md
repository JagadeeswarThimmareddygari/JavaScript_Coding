# JavaScritp_Coding
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
