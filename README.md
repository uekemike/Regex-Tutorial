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
| +                  | +?                   | Match one or more times.    | 
| ?                  | ??                   | Match zero or one time.     |
| { n }              | { n }?               | Match exactly n times.      |
| { n ,}             | { n ,}?              | Match at least n times      |
| { n , m }          | { n , m }?           | Match from n to m times.    |

The quantities n and m are integer constants. Ordinarily, quantifiers are greedy; they cause the regular expression engine to match as many occurrences of particular patterns as possible. Appending the ? character to a quantifier makes it lazy; it causes the regular expression engine to match as few occurrences as possible.

### Grouping Constructs
The subexpressions of a regular expression are defined by grouping constructs, while the substrings of an input string are captured by grouping constructions.
You can use grouping constructs to do the following:

- Match a subexpression that is repeated in the input string.

- Apply a quantifier to a subexpression that has multiple regular expression language elements. For  more information about quantifiers, see Quantifiers.

- Include a subexpression in the string that is returned by the Regex.Replace and Match.Result methods.

- Retrieve individual subexpressions from the Match.Groups property and process them separately from   the matched text as a whole.

### Bracket Expressions
What are bracket expressions in regex?
A bracket expression is either a matching list expression or a non-matching list expression. It consists of one or more expressions: ordinary characters, collating elements, collating symbols, equivalence classes, character classes, or range expressions.

Brackets indicate a set of characters to match. Any individual character between the brackets will match, and you can also use a hyphen to define a set.

- 'elephant'.match(/[abcd]/) // -> matches 'a'

You can use the ^ metacharacter to negate what is between the brackets. You will often see ranges of the alphabet or all numerals.

- 'donkey'.match(/[^abcd]/) // -> matches 'o'

Curly braces are used to specify an exact amount of things to match. They are used after an expression: \na{2}\ will only match ‘na’ exactly twice.

- 'panama'.match(/na{2}/) // -> no match
- 'banana'.match(/na{2}/) // -> matches 'nana'

### Character Classes
A “character class”, also called “character set”, can be used to tell the regex engine to match only one out of several characters. 

Simply place the characters you want to match between square brackets. If you want to match an a or an e, use [ae]. You could use this in gr[ae]y to match either gray or grey.

- [] denotes a character class

### The OR Operator
The 'Or' | operator (logical OR) is used to match characters or expression of either the left or right of the | operator. For example the (t|T) will match either t or T from the input string.

### Flags
The flag s means dot all. That is, it makes the . dot character (technically refered to as the wildcard character) match everything, even newlines. ... By default, the dot character in a regular expression matches everything, but newline characters. To get it to match newline characters as well, we are given the s flag.

As a quick example, suppose we need to make the expression /Hello/ search case-insensitively, that is, match either 'hello', 'HELLO', 'HeLLO', 'heLlo' and so on.

To do so we'll need to add the flag i in the regular expression as shown below:

/Hello/i


| Flag  | Name           | Modification                                      | 
|-------|----------------|-------------------------------------------------- |  
| i     | Ignore Casing  | Makes the expression search case-insensitively.   | 
| g     | Global         | Makes the expression search for all occurences.   | 
| s     | Dot All        | Makes the wild character . match newlines as well.|
| m     | Multiline      | Makes the boundary characters ^ and $ match the beginning and ending of every single line instead of the beginning and ending of the whole string.|
| y     | Sticky         | Makes the expression start its searching from the index indicated in its lastIndex property.|
| u     | Unicode        | Makes the expression assume individual characters as code points, not code units, and thus match 32-bit characters as well.|


### Character Escapes
The backslash character ( \ ) is the escaping character. It can be used to denote an escaped character, a string, literal, or one of the set of supported 

- The character that follows it is a special character,  For example, \b is an anchor that indicates that a regular expression match should begin on a word boundary, \t represents a tab, and \x020 represents a space.

- A character that otherwise would be interpreted as an unescaped language construct should be interpreted literally. For example, a brace ({) begins the definition of a quantifier, but a backslash followed by a brace (\{) indicates that the regular expression engine should match the brace. Similarly, a single backslash marks the beginning of an escaped language construct, but two backslashes (\\) indicate that the regular expression engine should match the backslash.

    - \t Matches a tab, \u0009.
    - \n Matches a new line, \u000A.
    
## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)