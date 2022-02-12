# Regex Tutorial - Matching a URL

Introductory paragraph (replace this with your text)

## Summary

This tutorial specifically covers regular expressions for matching a URL. The table of contents diplays everything that will be explaining about this type of regular expression.
A website name can only contain letters A-Z(capital or lowercase), the digits 0-9, a hyphen(-), and a period(.com). This is an example of a regular expression for matching a url.
```
EXAMPLE WILL GO HERE!!!
```

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors
Anchors do not match any characters, they match the position of a character(before or after).
The caret ^ matches at the beggining of the text while the dollar sign \$ matches and the end.
If the expression is "^s", then the text must start with an "s". If the expression is "d$", then the text must end with a "d".
```
Expression: ^s        start = match 
Expression: d$        end = match
```

### Quantifiers

### OR Operator

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

My name is Ahmed, I am a full-stack developer in training. I've enrolled in a coding bootcamp at UofT on a journey to learn website and mobile app development.

GitHub: https://github.com/AhmedAlkh

```
CODE BLOCK
```
[-a-zA-Z0-9.]{1,256}\.[a-zA-Z0-9]{1,6}\b([-a-zA-Z0-9.//]*)