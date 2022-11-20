// Design a function which can keep recieving the arguments on each function call and returns the sum when no argument is passed
// • // Example
// • sum(2)(4)(6)(1)(); // 13
// • sum(2)(4)(); // 6
// • sum(3)(); // 3

function sum(a){
return (b)=>{
if(!b){
return a;
}else{
return sum(a+b);
}
}
}

console.log(sum(2)(4)(6)(1)())

let factorial = memoize(function fact(value) {
return value > 1 ? value \* fact(value - 1) : 1;
});

factorial(5); // 120 (output is calculated by calling the function)
factorial(5); // 120 (output is returned from the cache which was stored from previous calculations)

function memoize(func){
const cache={};

    return (arg1)=>{
        if(cache.arg1){
            console.log("from cache.");
            return cache.arg1;
        }

        cache.arg1= func(arg1);
        console.log("from function calculation.")
        return cache.arg1;
    }

}

// Write a function that takes a string of parentheses and determine if the order of the parentheses is valid.
// The function should return true if the string is valid, and false if its invalid.

// “()” => true
// “)(()))”=>false
// “(“=>false
// “(())((()())())” =>true
function checkParenthesisValidity(stringOfParanthesis){
const stack=[];
const paranLen=stringOfParanthesis.length;
for(let i=0;i<paranLen;i++){
if(stringOfParanthesis[i]==="("){
stack.push("(");
}else{
if(stack.length>0 || stack[stack.length-1]==="("){
stack.pop();
}else{
stack.push(")");
}
}
}

    if(stack.length){
        console.log(false);
        return;
    }
    console.log(true);

}

checkParenthesisValidity("(())((()())())");
checkParenthesisValidity("(");

card1 card2 card3
image title image title image title
content content content

what will be the value of count
setState(count+1);
setState(count+1);
setState(count+1);

How many times component will rerender
function handleClick1() {
setA('aa');
setB('bb');
}

    function handleClick2() {
    Promise.resolve().then(() => {
      setA('aa');
      setB('bb');
    });

}
