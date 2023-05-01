# 17-Regex Tutorial: Email Matching

A regular expression is a sequence of characters that specifies a match pattern in text. This is an extremely powerful tool for a developer to validate user input, ensure the proper structure of data is being passed between methods or APIs, and can even help with securing websites from malicious users.

## Summary

The Regex I am researching today is an expression that can be used to validate proper email address structure. The sections below will break down each part of the expression to help gain a better understanding of how it works.

```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

## Table of Contents

- [17-Regex Tutorial: Email Matching](#17-regex-tutorial-email-matching)
  - [Summary](#summary)
  - [Table of Contents](#table-of-contents)
  - [Regex Components](#regex-components)
    - [Anchors](#anchors)
    - [Quantifiers](#quantifiers)
    - [Grouping Constructs](#grouping-constructs)
    - [Bracket Expressions](#bracket-expressions)
    - [Character Classes](#character-classes)
  - [Author](#author)

## Regex Components

### Anchors

* ```^```: The caret anchor tells the engine that this is the start of the string.
* ```$```: The $ anchor tells the engine that this is the end of the input string.

### Quantifiers

* ```+```: This quantifier matches the preceding character one or more times. 

### Grouping Constructs

* ```(...)```: This creates a capturing group, which allows us to capture the matched substring based on the contents inside. The Regex above contains three capturing groups.

### Bracket Expressions

* ```[a-z0-9_\.-]```: This is a character set which matches any character within the set. In this expression, it matches any lowercase letter, number, underscore, period or hyphen.
* ```[\da-z\.-]```: This is another character set which matches any number or lowercase letter, as well as period or hyphen.

### Character Classes

* ```.```: This matches any character except for a newline (```\n```).

## Author

Joseph Hayes is a University of Utah Bootcamp student who aspires to be a full-stack developer. 

[Joseph's Github](https://github.com/josephehayes/)