## Update dictionary in typescript

const object1 = {  
 a: 1,  
 b: 2,  
 c: 3  
};

const object2 = Object.assign({c: 4, d: 5}, object1);

console.log(object2.c, object2.d);  
// expected output: 3 5