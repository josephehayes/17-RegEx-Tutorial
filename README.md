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

Anchors are used for matching the position within a string, instead of matching a character like other components do. These are extremely useful to ensure the pattern matches the correct parts of a string.
The two anchors used in our email example are ^ and $.
* ```^```: The caret anchor tells the engine that this is the start of the string.
* ```$```: The $ anchor tells the engine that this is the end of the input string.

### Quantifiers

Quantifiers are used to match a certain number of occurences within the string. These are useful for more ambiguous matches, like matching for every space in a string, or for doing a greedy search (using ```*```).
The one quantifier in our example is the +.
* ```+```: This quantifier matches the preceding character one or more times. 

### Grouping Constructs

Grouping constructs are used to group sets of components together so that they can be treated as a single expression. In our example, this is used to group together matching for the beginning of an email address, then a domain, then a domain extension, which allows for multiple variations of emails and domains to be used, but requiring them all to follow the same structure.
* ```(...)```: This creates a capturing group, which allows us to capture the matched substring based on the contents inside. The Regex above contains three capturing groups.

### Bracket Expressions

Bracket Expressions are used to match a set of characters from the string within a pattern set within the square brackets (```[]```). 
* ```[a-z0-9_\.-]```: This is a character set which matches any character within the set. In this expression, it matches any lowercase letter, number, underscore, period or hyphen.
* ```[\da-z\.-]```: This is another character set which matches any number or lowercase letter, as well as period or hyphen.

### Character Classes

A character class is used to match any single character from a set of possible characters. The character classes in our example are generally contained within the Bracket Expressions, such as ```a-z0-9``` which matches any alphanumeric character, or ```\d``` which will match any digit.
* ```\.```: This character class matches any character except for a newline (```\n```), and is integral to many regex patterns.

## Author

Joseph Hayes is a University of Utah Bootcamp student who aspires to be a full-stack developer. 

[Joseph's Github](https://github.com/josephehayes/)
