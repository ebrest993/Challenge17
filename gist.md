# Understanding Regular Expressions

Regular Expressions are complicated bits of code that, if used properly and are well understood, can be made a great tool to have in one's toolbelt.

## Summary

The following is the code we'll be examining. This code will confirm the input to be a valid email format, complete with an "@" symbol and the ".com" or ".org" web address. The RegEx will be deconstructed and examined piece by piece.

The tutorial RegEx:
```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors

Anchors' jobs aren't to match characters, but rather to assert where in the engine the search takes place. Namely, the beginning or end of a string.

In the above example, the search will run at the beginning of the string, as shown by the `^` symbol at the start of the expression.

### Quantifiers

The quantifiers exist to determine exactly how many times an expression is repeated in a search.

In the above example, the quantifiers are the `+` symbols, which instructs to repeat an infinity number of times until finished.

### Grouping Constructs

Grouping constructs deal with smaller subsets of both the regular expression and the input string.

Here, the `(` and `)` group together the smallest sections of the expression to make sure they run within themselves.

### Bracket Expressions

Bracket expressions exist inside of opening and closing square brackets, and ultimately define a set of characters to search for.

The `[` and `]` brackets define different sets of characters required from the input.

### Character Classes

Character classes exist inside of the bracket expressions; they determine which specific characters will be searched for.

the `[a-z0-9_\.-]` gives us two classes: lowercase letters and any combination of numbers between 0 and 9.

### The OR Operator

'Or' operators allow the users to pick between one set of characters and another. 

The above does not contain an 'or' operator, but here's an example: 
```
(A||B),(C||D)
```
In this example, all of the following meet the requirements: 

`(A, C)`
`(A, D)`
`(B, C)`
`(B, D)`

### Flags

A flag determines if/when a regular expression will search in a different way.

### Character Escapes

Character escapes (indicated by a back slash) are used when you need to search for a specific character and, in doing so, rid it of any intrinsic coding-language value.

## Author

Elliott has been coding for roughly five months. He enjoys himself, though he has a long way to go.

GitHub: https://github.com/ebrest993