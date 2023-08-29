# Match HEX Values tutorial

## Summary

This will be used to match `HEX`` values:

`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

The description below will have details of each component used for this regular expression.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components

### Anchors

Anchor: `^`

Code snippet: `/^#`

Description: The Anchors by themselves, don't match regular expressions. They expand on the string based on expressions and matching patterns next to the anchor.
The `^` anchor is the beginning of a string that must match the character `#`.
The `#` is a hexadecimal number not a decimal number. `#` is always optional.

Anchor: `$`

Code snippet: `$/`

Description: This is the end of the string. Similar to the `^` anchor, `$` is used to check if a string matches a pattern. But `$` ends the string, not begins the string like the `^`.

### Quantifiers
Quantifier: `?`

Code snippet: `/^#?`

Description: `?` is a boolean value, 0 or 1. This makes the preceding symbol or character optional. In the regex, the quantifier `?` indicates that the character `#` is optional.

Quantifier: `{}`

Code snippet: `[a-f0-9]{6}`<br>
Code snippet: `[a-f0-9]{3}`

Description: 

`[A-Fa-f0-9]{6}` - This quantifier indicates how many times the pattern matches. This will search for a hex value with letters between a-f, A-F and digits from 0-9 stretching `{6}`  character spaces (example: abc123)

### OR Operator
OR Operator: `|`

Code snippet: `[a-f0-9]{6}|[a-f0-9]{3}`

Description: The `|` indicator (i.e. OR indicator) is a boolean that matches either the expression before or after. In our code snippet, a string with `{6}` characters containing lowercase a-f and/or integer between 0-9 OR the `{3}` character string containing lower case a-f and/or integer 0-9. A matching string has to have `{3}` or `{6}` characters with the specified pattern. Anything other than `{3}` or `{6}` characters will not match.

### Character Classes

Character Classes: `a-f, 0-9, A-F`

Code snippet: `a-f0-9`

Description: Character classes only match one out of several characters defined in the character set. A hyphen can be used inside a character class to define a range of characters. More than one range can be used -- as indicated in our code snippet.


### Grouping and Capturing

Grouping and Capturing: `()`

Code snippet: `([a-f0-9]{6}|[a-f0-9]{3})`

Description: The `()` groups the regular expression between them. This grouping treats multiple characters as a single unit. 
This group of data will be shown in the form of an array. This grouped expression is a bracket expression.

### Bracket Expressions
Bracket Expressions: `[]`

Code snippet:  `[a-f0-9]`

Description: Bracket expression is a regex that will match a specific pattern of characters. This includes alphabet, numeric, any special characters, symbols, etc. that are defined within the brackets. We use a hyphen `-` to describe a `set` or `range` of characters e.g. `[a-z]`.  You can also use `^` to negate between the brackets.

### Greedy and Lazy Match

Code snippet: `[a-f0-9]{6}`<br>
Code snippet: `[a-f0-9]{3}`

Description: *Greedy* means to `match the longest possible string`. *Lazy* means to `match the shortest possible string`.

## Author

My name is Melisha Evans. I am here to learn about full stack web development technologies. 
My GitHub profile is indicated below. Thank you for your time.

GitHub profile:  https://github.com/greentree31
