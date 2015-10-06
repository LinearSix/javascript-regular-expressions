## Regular Expressions in JavaScript

Objectives:

- Build a simple regular expression to parse CSS color values
- Create a search-and-replace regular expression to act as a simple typo checker

## What the heck are "regular expressions", anyway?

"Regular Expressions" is a term used to refer to a mini language-within-a-language that is commonly used for complex text parsing. Regular expressions go beyond JavaScript; once you learn basic regular expression syntax, you'll be able to use it to match and replace a variety of text with most modern programming languages, text editors, and development environments.

## Here's what it looks like

Here's a very simple example using JavaScript. Open up your favorite text editor and input the following lines of code:
```
var somestr = 'Regular Expressions are soooooo awesome!';
var regex = /so{6}\s/;
var matches = regex.exec(somestr);
console.log(matches[0]);
```
Save it as regex.js. Run it from the command line, and see the output with:
```
node regex.js
```

## Somebody tell me what just happened

You just wrote a little regular expression that matched the word 'soooooo' in the string 'Regular Expressions are soooooo awesome!', and logged the result to the console.

Let's break that down:

Line 1: You should already know what this does. 
Line 2: Creating a new variable using slashes as delimiters instantiates a new regular expression object using the text between the slashes as your regular expression. 
Line 3: The 'exec' method of your regular expression object takes one argument (the string that you want to run your regular expression on) and returns an array containing your match as the first element. If your regular expression didn't match the text, exec returns null.
Line 4: This should already look familiar to you by this point. This just displays the first element of the 'matches' array on the console.


## Awesome! What does the stuff between the slashes mean?

The stuff between the slashes is your regular expression. This example contains four "tokens":
- A lowercase 's'
- A lowercase 'o'
- {6} means that instead of matching the previous token, in the case 'o', match six 'o's in a row
- \s is a token that matches any whitespace character, in this case matching a space

All together, this means that your regular expression matches a lowercase 's' followed by six lowercase 'o's followed by a whitespace character. Since the string 'Regular Expressions are soooooo awesome!' contains exactly this ('soooooo '), .exec matches and returns the entire match as the first element of an array.

## What? When are we going to use this?

You are going to use this ALL THE TIME. Regular expressions are super-handy for pulling smaller strings out of large ones, like pulling the src attributes out of anchor tags in HTML documents, or pulling the video id from a YouTube video URL. Again, regular expressions go beyond JavaScript, so you'll be able to use this knowledge in other languages and places.

## Sweet! What else can we do with regular expressions?

You've already seen three types of regular expression tokens:
- basic tokens that match the characters they represent ('s', 'o')
- repetition quantifiers that modify the preceding token by repeating it ({6})
- character classes that match more than one character (\s)
