### Q1. Flatten Array: [[[[1,1.1]],2,3],[4,5]]; 
Output: [1,1.1,2,3,4,5]

Ans: 
```
function falttenArray(arr) {
  const result = [];
  arr.forEach((element) => {
    if(Array.isArray(element)){
      const nestedArray = flattenArray(element);
      result.push(...nestedArray);
    }
    else {
      result.push(elem);
    }
  });
  return result;
}
console.log(falttenArray([[[[1,1.1]],2,3],[4,5]]));
```

### Q2. Reverse a string with decrementing loop: 'My name is John Doe'.
Output : 'eoD nhoJ si eman yM'

Ans:
```
function reverseString(str) {
  var newString = '';
  for (var i = str.length - 1; i >= 0; i--){
    newString += str[i];
  }
  return newString;
}
console.log('My name is John Doe');
```

### Q3. Check weather a String is palindrome or not: 'ABCDCBA', 'MADAM'.
Output: 'ABCDCBA' is Palindrome, 'MADAM' is Palindrome, 'BANANA' is not Palindrome

```
function isPalindrome(str) {
  let revStr = '';
  for(let i = str.length - 1; i >= 0; i--){
    revStr += str[i];
  }
  if(revStr == str) {
    console.log(`${str} is Palindrome`);
  }
  else {
    console.log(`${str} is not Palindrome`);
  }
}

isPalindrome('ABCDCBA');
isPalindrome('MADAM');
isPalindrome('BANANA');
```

### Q4. Check number is Palindrome or not: '1221', '2233'.
Output: 1221 is Palindrome, 2233 is not Palindrome.

```
function checkNumberPalindrome() {
  let num = window.prompt('Enter Number: ');
  let originalNum = num;
  let reverse = 0;
  while(num != 0) {
    reverse = (reverse * 10) + (num % 10);
    num = parseInt(num / 10);
  }
  if(originalNum == reverse) {
    console.log(`${originalNum} is Palindrome`);
  }
  else {
    console.log(`${originalNum} is not Palindrome`);
  }
}
checkNumberPalindrome();
```

### Q5. Check number of Duplicates in an Array: [1,4,5,2,3,6,1,3]
Output: 2

```
function numberOfDuplicate(arr){
    let count = 0;
    for(let i = 0; i < arr.length; i++) {
        for(let j = i+1; j < arr.length; j++){
            if(arr[i] == arr[j]){
                count++;
            }
        }
    }
    console.log(count);
}
numberOfDuplicate([1,4,5,2,3,6,1,3]);
```

### 
