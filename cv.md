# Gurinovich Ilya # 

## Contacts: ##
* **Phone:** +375445878506
* **Email:** gurinovich-ilya@list.ru
* **GitHub:** Bobotet 

## About me: ##

I’m a second-year student of BNTU. During the first course I independently studied the front-end. Now I decided to try my hand at this course.
I'm wondering how far I can go in this course and, if I can complete it, will I get a job

## Skills: ##
* HTML
* CSS/SASS
* JS
* Git, GitHub
* VS Code
* BEM
* Firgma, Marsy

## Code Example: ##
### __Task from codewars:__

A format for expressing an ordered list of integers is to use a comma separated list of either
individual integers
or a range of integers denoted by the starting integer separated from the end integer in the range by a dash, '-'. The range includes all integers in the interval including both endpoints. It is not considered a range unless it spans at least 3 numbers. For example "12,13,15-17"
Complete the solution so that it takes a list of integers in increasing order and returns a correctly formatted string in the range format.

Example:

solution([-10, -9, -8, -6, -3, -2, -1, 0, 1, 3, 4, 5, 7, 8, 9, 10, 11, 14, 15, 17, 18, 19, 20]);
// returns "-10--8,-6,-3-1,3-5,7-11,14,15,17-20"
```
function solution(list){
  let first = true;
  let firstIndex = 0;
  let lastIndex = 0;
  let sequence = false;
  let res = '';
  for(let i = 0; i < list.length; i++){
    if(first && list[i + 1] === list[i] + 1 && list[i + 2] === list[i + 1] + 1){
      firstIndex = i;
      lastIndex = i + 2
      first = false;
      sequence = true;
      i = lastIndex - 1;
    }
    else if(list[i + 1] === list[i] + 1 && sequence){
        lastIndex = i + 1;
    }
    else if(sequence){
      res += `${list[firstIndex]}-${list[lastIndex]},`;
      first = true;
      sequence = false;
      list.splice(firstIndex, lastIndex - firstIndex + 1)
      i -= lastIndex - firstIndex + 1
    }
    else{
      res += `${list[i]},`;
    }
 }
  res = String(res)
  res = res.split('');
  res.pop()
  return res.join('')
}
```

## Experience: 

## Education: 
* Belarusian National Technical University
* Self education

## English level: A2