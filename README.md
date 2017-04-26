## JavaScript crash course

#### Primitives (basic values)
#### There are a few basic types of values you can have in JS: 
##### *Strings*: Any combination of text (text must be inside either "" or '')
```javascript
"Course: Coding for Managers"
"2017"
"April 26, 2017"
"Today is Wednesday, April 26, 2017"
"My name is Eric."
```
##### *Numbers*: Integers, Decimal values etc. (For doing mathematical operations)
```javascript
5
5.5
10000000
3.1415926535
```
###### You can manipulate strings and numbers with some basic 'operators': 
###### Concatenate (join) strings together with `+`:
```javascript
"Hello: My name is " + "Eric."
```
###### Usual things with math operators `+ - /` etc.:
```javascript
5 + 5
6 - 1
9 * 9 
//Modulo (Remainder from your elementary school math class)
10 % 5 // 0 
15 % 6 // 3
10 % 3 // 1
```

##### Booleans and Logic
```javascript
true 
false 
```
###### Examples 
```javascript
var five = 5; 
five === 5 // true (=== strict equality. Compares two values to see if they're equal)
five === 6 // false 
five > 4 // true 
five < 3 // false 
```

###### More logic operators: 
```javascript
true && false // AND operator. This examples is false (both values need to be true)
true || false // OR operator. This example is true, since at least one of the two values are true
true && true && (1 === 2) //false 
false || false || (1 === 1) // true
```
#### Some JS code: 
```javascript
var num = 5; 

if (num < 10) {
	alert(num + " is less than 10!"); 
}
```

#### Wrap the above in reusable code! (AKA a function)
```javascript
function lessThan10(num) {
    if (num < 10) {
        alert(num + " is less than 10!")
    } else {
        alert(num + " is NOT less than 10!")
    }
} 
```
#### Call the function (AKA use the function)
```javascript 
lessThan10(5)

lessThan10(25)

```


#### Objects and more complicated types (composite)

```javascript
var anArrayOfNumbers = [1, 3, 5, 7]; 

var objectFormat = {
    property1 : value1, 
    property2 : value2, 
    //and so on...
}; 

var meAndMyself = {
    name: "Eric L.",
    birthday: "April 7",
    eyeColor: "brown",
    gender: "m",
    over18: true,
}; 

var printBio = function(person) {
    var pronoun; 
    
    if (person.gender === "m") {
        pronoun = "He"; 
    } else if (person.gender === "f") {
        pronoun = "She"; 
    }
    
    alert(person.name + " was born on " + person.birthday + ". " + pronoun + " has " + person.eyeColor + " eyes.")
}; 

printBio(meAndMyself); 
