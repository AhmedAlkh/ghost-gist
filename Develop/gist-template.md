# Regex Tutorial - Matching a URL

This is a regular expressions tutorial on matching a URL. 
The expression will define criteria that an input must meet in order for the input to be accepted as a URL. 
You can also create regular expressions for other things such as hex codes, email addresses, and html tags. 
We will be focusing specifically on a regular expression for a URL.

## Summary

This tutorial specifically covers regular expressions for matching a URL. 
The table of contents diplays everything that will be explained about this type of regular expression.
A website name can only contain letters A-Z(capital or lowercase), the digits 0-9, a hyphen(-), and a period(.com). 
This is an example of a regular expression for matching a url.
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
The caret ^ matches at the beggining of the text while the dollar sign \$ matches at the end.
If the expression is "^s", then the text must start with an "s". 
If the expression is "d$", then the text must end with a "d".
```
Expression: ^s        start = match 
Expression: d$        end = match
```

### Quantifiers

Quantifiers indicate the number of characters or expressions to match. 
With a quantifier you can specify how many characters you want the expression to find.
```
\d{6} - accepts 6 or more digits(\d represents digits 0-9, {6} represents the length)
\b\d{6}\b - accepts 6 digits(no more or less, \b sets the restrictions)
\b\d{3,6}\b - accepts 3-6 digits(length of 3,4,5, or 6 accepted. No more or less)
```

### OR Operator

The OR operator is similar to the use of OR in a for loop, it is denoted with a vertical line character (|).
The OR operator allows the expression to choose from multiple options if one of the options matches.
```
blue|grey|red - Blue OR grey OR red would be accepted.
```

### Character Classes

A character class is a special notation that matches any symbol from a certain set.
The most common character classes are: 
* \d ??? digits.
* \D ??? non-digits.
* \s ??? space symbols, tabs, newlines.
* \S ??? all but \s.
* \w ??? Latin letters, digits, underscore '_'.
* \W ??? all but \w.
* . ??? any character if with the regexp 's' flag, otherwise any except a newline \n.
```
Expression: \D
Input: 123A456
In this input, the expression would find the 'A'.
```

### Flags

Flags are optional parameters to a regular expression that will modify the search.
A flag is denoted using a single lowercase alphabetic character.
There are 6 flags:
* i (Ignore Casing) - The search is not case sensitive
* g (Global) - Search for all occurrences on a global scope
* s (Dot all) - Makes the wild character . match newlines as well
* m (Multiline) - Boundary characters ^ and $ match the beginning and ending of every single line.
* y (Sticky) - Expression starts searching from the index indicated in its lastIndex property.
* u (Unicode) - Expression assumes individual characters as code points, not code units, thus matching 32-bit characters as well.


### Grouping and Capturing
Grouping and capturing refers to the use of parentheses to seperate groups within a regular expression.
A whole regular expression can be broken into parts which allows the expression to get part of the match
as a seperate item in the result array. If there is a quantifier after the parentheses, it applies to the contents
of the parentheses as a whole.
```
^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$
 (     1     ) (     2     )  (     3      )(     4     )
```
### Bracket Expressions

[] Brackets indicate a set of characters to match. 
Any individual character within the brackets will match. 
{} Curly braces specify the amount of things to match.
```
^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$
                [   ^    ]            { ^ }
               [a-z, ., -]   {at least 2, no more than 6}
```

### Greedy and Lazy Match

Greedy will try to match the longest string, lazy will try to match the shortest string.
A greedy match will match the whole string that is accepted including everything inbetween,
a lazy match will break up the string to only find specifically what it searches for.
```
Greedy expression: /".+"/g                                 Lazy expression: /".+?"/g
Input: 'this will "find" the words "in" double quotes'     Input: 'this will "find" the words "in" double quotes'
Greedy result: "find" the words "in"                       Lazy result: "find", "in"
```
### Boundaries

The boundary is set by \b at the beggining and end of the expression. 
It makes it so that the expression will not continue to search beyond the search parameters.
the boundary says to the expression "we have found what we are searching for, stop searching"
```
\b\d{6}\b - will accept 6 digits, no more or less.
```
### Back-references

When defining back-references, you can reuse and reference previous groups in the expression.
Groups are referenced by the order which they are placed in the expression.
* (group 1 is \1)(group 2 is \2)(group 3 is \3)
```
Expression: /(['"])(.*?)\1/g 
             ( \1 )      ^
             references group 1
```

### Look-ahead and Look-behind

Look-ahead and look-behind are useful in instances when we need to match something depending on the context before or after it. 
 "Look-ahead" and "look-behind" together are referred to as "lookaround".
```
X(?=Y) - matches X if followed by Y
X(?!Y) - matches X if not followed by Y
(?<=Y)X - matches X if after Y
(?<!Y)X - matches X if not after Y
```

## Author

My name is Ahmed, I am a full-stack developer in training. 
I've enrolled in a coding bootcamp at UofT on a journey to learn website and mobile app development.

GitHub: https://github.com/AhmedAlkh