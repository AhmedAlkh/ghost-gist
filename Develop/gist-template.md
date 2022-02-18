# Regex Tutorial - Matching a URL

This is a regualar expressions tutorial on matching a URL. The expression will define criteria that an input must meet in order for the input to be accepted as a URL. You can also create regular expressions for other things such as hex codes, email adresses, and html tags. We will be focusing specifically on a regular expression for a URL.

## Summary

This tutorial specifically covers regular expressions for matching a URL. The table of contents diplays everything that will be explaining about this type of regular expression.
A website name can only contain letters A-Z(capital or lowercase), the digits 0-9, a hyphen(-), and a period(.com). This is an example of a regular expression for matching a url.
```
^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$
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

Quantifiers indicate the number of characters or expressions to match. With a quantifier you can specify how many characters you want the expression to find.
```
\d{6} - accepts 6 or more digits(\d represents digits 0-9, {6} represents the length)
\b\d{6}\b - accepts 6 digits(no more or less, \b sets the restrictions)
\b\d{3,6}\b - accepts 3-6 digits(length of 3,4,5, or 6 accepted. No more or less)
```

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