## Regular Expressions in JavaScript

Objectives:

- Build a simple regular expression to parse CSS color values
- Create a search-and-replace regular expression to act as a simple typo checker

## What the heck are "regular expressions", anyway?

"Regular Expressions" is a term used to refer to a mini language-within-a-language that is commonly used for complex text parsing. Once you learn basic regular expression syntax, you'll be able to use it to match and replace a variety of text with most modern programming languages, text editors, and development environments.

## Here's what it looks like

Here's a very simple example using JavaScript. Open up your favorite text editor and input the following lines of code:
```
var somestr = 'Regular Expressions are soooooo awesome!';
var regex = /so{5}\s/;
var matches = regex.exec(somestr);
console.log(matches[0]);
```
Run it, and see the output.


## Somebody tell me what just happened


