# Regex Tutorial

Regex, short for regular expression, is a powerful tool for creating patterns that enable the identification, location, and manipulation of text. In applications like the VS Code text editor, where you search for specific words or numbers using Ctrl + F, you can leverage regex by selecting the .* button on the right-hand side. This functionality allows for more flexible and sophisticated text searches based on user-defined patterns. To illustrate, let's delve into a detailed example to better understand how regex works.

## Summary

The Featured Regex for this Tutorial to verify that user input is a valid email address:

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

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

Regex components are fundamental building blocks that make up regular expressions, allowing users to create patterns for matching, locating, and manipulating text. Here are some common regex components:

### Anchors
-`^` (caret): The first thing seen in the matching email snippet above is ^. This means beginning so it means email should start with `([a-z0-9_\.-]+)` expression.</br>
-`$` (dollar): The last thing seen is $. It means end of the email address. So the email should end with `([a-z\.]{2,6})`
### Quantifiers

### Grouping Constructs

### Bracket Expressions

### Character Classes

### The OR Operator
The `|` (pipe) in this expression is an OR operator. The regex engine will try to match the pattern on the left side of the `|`, and if that doesn't work it will try to match the pattern on the right side. For example if `abc | dfg`, both `abc` and `dfg` match
### Flags
A flag in regex is a modifier or option specified after the closing delimiter (typically a forward slash `/`). It influences the behavior of the regular expression pattern. Flags can be used to control aspects such as case sensitivity, global matching, and multiline matching. In this example `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` the flags `/` are applied in a defualt mannder, which typically means it is case-sensitive. No additional flags like `/g` for global matching or `/i` for case-insensitivity are present in this regex.

### Character Escapes

## Author

Nicholas Vacca

Deployed Github-Gist Link:

Github Repository: https://github.com/magellanrose/Regex_Tutorial 
