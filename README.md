# Regex Tutorial

Regex is short for Regular Expression. These are not necessarily javascript based or belonging to any other programming language. Put simply, they are a sequence of characters that define a search patern. For example, the following can be used to validate an email: 

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`


## Summary

In the following tutorial I will be defining and explaining the expression used to match Hex values. The code for this is as follows:


`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`


## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions and Character Classes](#bracket-expressions-and-character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)

## Regex Components

### Anchors
First off, we need to explore anchors. ^ and $ are both considered anchors. The ^ anchors says that whatever string is being searched for begins with the character that follows it. The $ anchor, similarly, says that the string being searched for ends with the character that preceeds it. You can see these characters being used in the example expression. 

In other words, they define the start and end of the expression.

`/^ ---expression--- $/`

NOTE: REGEX IS CASE SENSITIVE


### Quantifiers

Quantifiers, as the name implies, are used to quantify how many instances of a character, group, or character class must be present in the input for a match to be found. 

`* -> Match zero or more times`

`+ -> Match one or more times`

`? -> Match zero or one times`

Alternatively, {n} can be used to specify an exact ammount of times to be matched where n is the number of times. The expression {n,m} can be used to specify and range of times for the match to be found.

In this portion of the above expresion, `[a-f0-9]{6}`, the {6} is saying that `[a-f0-9]` should be found 6 times.


### Grouping Constructs

Grouping constructs delineate the subexpressions of a regular expression and capture the substrings of an input string. This can be used to search for multiple instances of an expression, for example.

`([a-f0-9]{6}|[a-f0-9]{3})`

This part of the expression is grouped together.


### Bracket Expressions and Character Classes

Brackets indicate a set of characters to match. For example, putting `[ae]` in the word `gr[ae]y` will return either "grey" or "gray".

In the example expression we can seen this being used here: `[a-f0-9]`
This part of this expression is saying find any character that falls between "a" and "f" and then any digit that falls between "0" and "9"


### The OR Operator

The OR operator, as the name implies, look for one expression OR another. In the example expression we can see this being used here: 

`([a-f0-9]{6}|[a-f0-9]{3})`

So this says "search `[a-f0-9]{6} OR [a-f0-9]{3}`


### Flags

Flags are not used in the expression but they are still good to know. A flag is an optional parameter to a regex that modifies its behavior of searching. 

`i -> Ignores casing (AKA case insensitivity)`

`g -> Global, search for all occurances`

`s -> Dot All, "." matches new lines as well`

`m -> Multi-line`

`y -> Sticky. Start search at last instance`

`u -> Unicode. Expression assumes individual character as code points and not code units and this matches 32-bit characters as well`


## Author

Walker Jezek

[Github](https://github.com/walkerjezek)

[LinkedIn](https://www.linkedin.com/in/walker-jezek-bb788958/)
