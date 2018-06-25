# Naming-Convention

In computer programming, a naming convention is a set of rules for choosing the character sequence to be used for identifiers which denote variables, types, functions, and other entities in source code and documentation. Naming conventions make programs more understandable by making them easier to read. They can also give information about the function of the identifier-for example, whether it's a constant, package, or class-which can be helpful in understanding the code.


## Uppercase

A `constant` is a variable with a static value, that won't change. For example, if your project required the need to multiply a value by the state tax, you might assign this rate, $0.08 to a constant. However, not all languages have these variable types built in. As such, it's a best practice to use all capital letters to remind yourself that you're working with a constant. This is a common convention in the JavaScript world, and is used its native objects, like MATH.PI

```JavaScript
var TAXRATE = 0.08;
```

## Hungarian notation

You've surely, at some point, come across a variable that was proceeded by a single letter, such as "s" or "i". Hungarian notation is a naming convention that reminds the developer about the type of variable that he's working with: string, integer, etc. Particularly in the JavaScript world, this practice is frowned upon, due to the fact it's a loosely typed language. A loosely typed language is one that doesn't require you to declare the data type of a variable. Why is that significant? What if, using the notation convention above, we declared a string with the "s" prefix, but then later changed the variable to an integer? At that point, this form of notation would in fact work against us, not for us. 

Developers also use this method to describe variables that have acces to certain libraries or frameworks, for example jQuery or lodash.

```JavaScript
// s for String
var sName = 'Jon Snow'; 

// i for Integer
var iBirthYear = 1980;

// $ for jQuery
var $container = $('#container');

// _ for lodash
var _isEqual = _.eq('a', 'a');
```

## Capital First Letter 

Class names should be nouns, in mixed case with the first letter of each internal word capitalized. Try to keep your class names simple and descriptive. Use whole words-avoid acronyms and abbreviations. In JavaScript, we don't really have classes; but we do have constructor functions. The reason why we capitalize the name of the constructor (Person) is because it can prove easy to sometimes forget the new keyword. The capitalization is a helpful alert for the developer, when debugging.

```JavaScript
function Person(first, last) {
    this.firstName = first;
    this.lastName = last;
}

var person = new Person("Jon", "Snow");
```

## CamelCase vs under_score

 Why is it that some variables use a camelCase pattern,while others use an underscore to separate words? What's the correct method? The answer is there is no correct usage. It entirely depends on the language, and/or your company's coding conventions. Both are perfectly acceptable.

```JavaScript
var firstOfHerName = 'Daenerys of the House Targaryen';

var first_of_her_name = 'Daenerys of the House Targaryen';
```

However, with all that said, it's a best practice -- when you have the option -- to follow the common conventions of the language you're using. For example, the large majority of JavaScript developers use the camelCase syntax, while other languages, like PHP, tend to prefer the underscore usage. Though, again, this isn't set in stone. The Zend Framework advocates camelCasing as a best practice.

> More important than what you use is ensuring that you stick to it!

## Underscore before first letter

It's simply a naming convention that reminds the developer that the variable/property/method is either private or protected, and cannot be accessed from outside of the class.

```PHP
private $_someVariable;
```
