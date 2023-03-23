# Regex Tutorial
This tutorial will explain the basics of Regex, or regular expression, and go over a specific case.

## Summary
Two common regex for matching an email are:\
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`   \
I chose this regex for an email because it seems to be the most common and useful.

## Table of Contents

- [Anchors](#anchors)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)
- [Summary](#summary)

## Regex Components
These are the building blocks of a regex component and there are many different components that are useful and we will get into what they are and do below. The ones that are used in the example regexes are `^, /, a-z, 0-9, (), [], @, \., _, -, +, \d, {2,6}, $`.

### Anchors
`^` and `$` are anchors. `^` meaning that the string starts with the following group and `$` meaning that it ends with the previous group

### Grouping Constructs
Group constructs are collections of components that are well... GROUPED together to indicate a collection of certain characters we want to look for.\
Let's cut up our regex into group constructs and get rid of the anchors: \
`([a-z0-9_\.-]+)`, `([\da-z\.-]+)`, `([a-z\.]{2,6})` \
We also have these outside of groups: `@`, `\.` \
As you can see parenthesis:`()` denotes a group but about the components outside of the groups? That just means that it's a single character and not a group.

### Bracket Expressions
Inside of the group are square brackets `[]` which are essentially an array meaning that as long as the string includes some of the characters inside it passes

### Quantifiers
`*` means the preceding character or group can be mathced 0 or more times while `+` is matched at least once. Curly brackets quantify the allowed length of the array. In our case: `{2,6}` means 2 to 6 characters long. 

### Character Classes
`a-z` means any lowercase letter and `A-Z` is any uppercase letter and you can probaly guess that `0-9` is any number from 0 to 9. Note that `\d` is the same as `0-9` There are also dashes, `-`, and underscores, `_`. 

### The OR Operator
The email regex does not use it but a vertical line `|` is an or so the string can contain either side of the line.

### Flags
Flags are not used in this regex but they go after the last backslash. 

### Character Escapes
The backslash, `\`, is a character escape used to specify a period in the string and not a `.` as a character class that means any character.

### Summary
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`   \
So all together we have `/^` meaning that the following needs to be the first thing, `([a-z0-9_\.-]+)` meaning the group must contain any letter or number, underscores, periods, and dashes. Then a @ that's in all emails. The second group is the same as the first but cannot contain underscores. A period followed by any group of letters between 2 and 6 long.

## Author
Written by: Zechariah Barrett\
[Email](zechariahbarrett@outlook.com)\
[Github](https://github.com/ZechB7)
