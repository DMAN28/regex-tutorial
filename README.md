# regex-tutorial
# The Fundamentals of regular expressions

The following was written with the intention of helping the reader better understand REGEX. To simply put it, regular expressions (REGEXS) are a pattern notation that allows the user to describe and parse text. 

## Summary
Regular expressions have many applications. One of the most common is checking for password constraints. The regular expression gives us the ability to enforce these constraints by checking them in any order, whether a digit letter or special character comes first or last. The following REGEX is used to verify a strong password.

(?=^.{6,}$)((?=.*\w)(?=.*[A-Z])(?=.*[a-z])(?=.*[0-9])(?=.*[|!"$%&\/\(\)\?\^\'\\\+\-\*]))^.*

 In our example these would be the constraints applied to the password. 

(?=^.{6,}$)	Require that password to have a minimum length of 6.
(?=.*[0-9])	Require at least one digit.
(?=.*[a-z])	Require at least one lowercase letter.
(?=.*[A-Z])	Require at least one uppercase letter.
(?=.*[|!"$%&\/\(\)\?\^\'\\\+\-\*])    Require that at least one special character appear anywhere in the string.


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
Anchors are the start and end it defines the where the string begins and the characters that follow it.  The caret ^ will match the position before the first character in the string. Where as the $ will match right after the last character in the string. ^.{6,}$ 

### Quantifiers
Quantifiers set the limits of the string that your regex matches they will generally set the max and min characters that you are searching for. In the following example {6,} it is setting the limit of 6 characters.

### OR Operator
The OR operator is used when you want to match the character of either the left side or right.

### Character Classes
Character classes set the character or charters the match or use. In this piece of code (?=.*\w) the .*\w is is to match any character except for line terminators and match any word character (equivalent to [a-zA-Z0-9_])

### Flags
A flag will set  a parameter which changes the behavior of the regular expression. There are six different flags that can be used the the most common ones are.

i— With this flag the search is case insensitive.

g— Global search returns all results without only the first result is returned.

m— Multi-line search input string should be treated as multiple lines. Without this, multi-line strings match the beginning and end of each line.

### Grouping and Capturing
Regular expressions inside round brackets and parentheses are considered a grouping this indicates the group and range of expression characters. In this example we have a grouping that is looking for (?=.*[A-Z]) uppercase letters then another grouping (?=.*[a-z]) this one looking for lowercase. 

### Bracket Expressions
Bracket expression represent a range of characters that we are looking to match. In our example [A-Z] we are setting a range of characters we want to match specifically A through Z with a capital letter.

### Greedy and Lazy Match
A greedy quantifier will match as many occurrences as possible. Where as Lazy quantifier will repeat a minimal number of times. 

### Boundaries
Boundaries indicate the beginnings and endings of lines and words. They do not match any characters. Instead it will match at certain positions anchoring the regular expression and match at those positions.

### Back-references
Back references are used to ID and match the same text as previously matched by a capturing group.

### Look-ahead and Look-behind
In this example we have a positive look ahead (?=^.{6,}$. The positive look ahead ?= will try and match the pattern in the lookahead. If it can match then the regex will proceed with matching the rest of the pattern. If it cannot then the match is discarded.

## Author

If you have any questions fee free to reach out DMAN28 or at : dmanriqu@my.chemeketa.edu.
