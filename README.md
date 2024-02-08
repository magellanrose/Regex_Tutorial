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
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` In this regex expression there is the `+` which applies to the username part of the email address. The `+` can be used in the `()` like `([a-z0-9_\.-]+)` this example which applies to the domain part of the email address. `{2,6}` applies to the top level domain part of the email address. These quantifiers help define the structure of the email address in terms of the number of allowed occurrences for specific character sets. The `+` quantifier allows for flexibility in the lengths of the username and domain parts, while `{2,6}` restricts the TLD to between 2 and 6 characters.

### Grouping Constructs
Grouping constructs in regular expressions enable the consolidation of multiple characters into a cohesive unit, establishing subexpressions within the overarching pattern. These constructs fulfill diverse roles, such as facilitating the application of quantifiers to a character group, capturing specific segments of the matched text for future reference, and specifying alternatives within a defined scope. The primary and widely used grouping construct is represented by parentheses (). So in the example provided `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` we have `([a-z0-9_\.-]+)`, `([\da-z\.-]+)`, `([a-z\.]{2,6})` all seperated by grouping constructs.

### Bracket Expressions
Bracket expressions, also known as character classes, are used to define sets of characters that can match at a particular position in the string. In most regex expressions, you define a character class using square brackets `[]`. Bracket expressions can also be known as character classes.

### Character Classes
`[a-z0-9_\.-]+` This character class is used to define valid characters for the username part of the email address. `[\da-z\.-]+` This character class defines valid characters for the domain part of the email. The `+` outside the character class means that one or more of these characters should be present. `[a-z\.]{2,6}` This character class is used for the top-level domain part of the email address. The `{2,6}` specifies that there should be between 2 and 6 characters in this set.

### The OR Operator
The `|` (pipe) in this expression is an OR operator. The regex engine will try to match the pattern on the left side of the `|`, and if that doesn't work it will try to match the pattern on the right side. For example if `abc | dfg`, both `abc` and `dfg` match.

### Flags
A flag in regex is a modifier or option specified after the closing delimiter (typically a forward slash `/`). It influences the behavior of the regular expression pattern. Flags can be used to control aspects such as case sensitivity, global matching, and multiline matching. In this example `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` the flags `/` are applied in a defualt manner, which typically means it is case-sensitive. No additional flags like `/g` for global matching or `/i` for case-insensitivity are present in this regex.

### Character Escapes
There are a few character escapes in this regex expression `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`. `\.` is used to match a literal dot `.`. In regular expressions, a dot by itself has a special meaning and matches any single character. By using `\.` instead, the regex ensures that it matches an actual dot character. The escape sequence `\d` is a shorthand for matching any digit (equivalent to the character class `[0-9]`). In this regex, `[\da-z\.-]+` is used to match the domain part of the email address, allowing digits, lowercase letters, dots, and hyphens. The escape sequence `\w` is a shorthand for matching any word character (equivalent to the character class `[a-zA-Z0-9_]`). In this regex, `[a-z0-9_\.-]+` is used to match the username part of the email address, allowing lowercase letters, digits, underscores, dots, and hyphens. These escape sequences start with a backslash \ followed by a character or a combination of characters. Here are some other common character escapes: `\D` Matches any non-digit. `\W` matches any non-word character. `\s` matches any whitespace character. `\S` matches any non-whitespace character. By employing character escapes, you can precisely define which characters you want to match and avoid any unintended interpretations of special characters in your regular expressions. This flexibility allows you to craft regex patterns that accurately meet your specific matching requirements.

## Author

Nicholas Vacca

Deployed Github-Gist Link:

Github Repository: https://github.com/magellanrose/Regex_Tutorial 
