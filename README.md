# Regex - Regular Expressions

Developers write code, but they also *write about code*. 

Objective of this tutorial is to explains how a specific regular expression can be used, by breaking down each part of the expression and describing what it does.

A regular expression (or "regex") is a search pattern used for matching one or more characters within a string.

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

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
- Matching Fixed Strings
- Matching Special Characters
- Matching Character Sets
- Specifying Groups and Fields
- Evaluating Occurrences
- Specifying Location
- Specifying Alternatives
- Matching Information from a Table
- Capturing Multiple Lines
- Managing the Scope of Analysis

### Anchors

### Quantifiers
Quantifiers specify how many instances of a character, group, or character class must be present in the input for a match to be found.


| Greedy quantifier  | Lazy quantifier      | Description                 | 
|--------------------|----------------------|-----------------------------|  
| *                  | *?                   | Match zero or more times.   | 
| +                  | +?                   |Match one or more times.     | 
| ?                  | ??                   | Match zero or one time.     |
| { n }              | { n }?               | Match exactly n times.      |
| { n ,}             | { n ,}?              | Match at least n times      |
| { n , m }          | { n , m }?           | Match from n to m times.    |

The quantities n and m are integer constants. Ordinarily, quantifiers are greedy; they cause the regular expression engine to match as many occurrences of particular patterns as possible. Appending the ? character to a quantifier makes it lazy; it causes the regular expression engine to match as few occurrences as possible.

### Grouping Constructs

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)