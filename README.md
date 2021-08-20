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
   console.log(largest)
   console.log(secondlargest)
}

secondLargest([2,3,4,6,6,5])
```
