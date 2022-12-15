# Learning Regex

This gist is an exercise to teach myself Regular Expressions (Regex). Following tutorials provided and independent research I intend to identify the components of Regex expression. Additionally, I will choose an expression from a list provided and breakdown and analyze a Regex expression.

## Summary

* Matching a Hex Value: `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

This expression is designed to match a hex code for a color. The statements begins with an ``^`` anchor followed by ``#`` which means it wants to match
with a string beginning with the 'hashtag' symbol. The ``?`` quantifier shows that it is intending to match with 0 or more characters in the proceeding statement. The following parentheses indicate a capture group that creates two sub-expressions. The first sub-expression ``[a-f0-9]{6}`` is looking for characters 'a' through 'f' and zero through nine and is followed by the quantifier ``{6}`` which means it will match six characters in the preceding ranges. The sub-expressions are separated by ``|`` the or operator, which means that the expression is looking to match the preceding sub expression or the following sub-expression. On to the second sub-expression ``[a-f0-9]{3}``, like the last sub expression it is looking for characters 'a' through 'f' and zero through nine. However, this sub-expression is only looking to match three characters instead of six. Finally, the expression ends with an ``$`` anchor which matches the end of a string. 

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

``^ and $`` are anchor characters with ``^`` signifying the beginning of a string and ``$`` signifying the end of the string.

### Quantifiers

Quantifiers modify the previous character in a regular expression to state how many of those characters in a row are being searched for.

### OR Operator

The OR operator (``|``) separates characters contained within groups when either/or character is accepted in the search.

### Character Classes

Defines a set of characters any one of which occurring in a sting will be accepted as a match.

### Flags

Flags are placed at the end of a regex statement, after the second slash. they define the functionality/limits to statement and are optional.

### Grouping and Capturing

Grouping is done primarily by using parentheses ``()`` to create sub-expressions.


### Bracket Expressions

 Characters that appear between square brackets ``[]`` and represent a range of characters that we want to match.


### Greedy and Lazy Match

Greedy searches match the longest possible sting, syntax (``.+``). Lazy matches match the shortest possible string and are enabled by placing a ``?`` after a quantifier. ex: (``*? / +? / ??``) 

### Boundaries

Denoted with ``/b`` for a word boundary and ``/B`` for not-a-word boundary. Word boundaries matches positions where one side is a word character (usually a letter, digit or underscore. Not-a-word boundaries match where word boundaries do not, when neither side is a word character.

### Back-references

Back-references are regular expression commands which refer to a previous part of the matched regular expression and are denoted by a backslash ``\`` and a single digit. ex: ``('\1')`` 

### Look-ahead and Look-behind

Lookahead allows to add a condition for “what follows”, syntax is ``X(?=Y)``. Lookbehind is similar, but it looks behind, syntax is ``(?<=Y)X``

## Author

Bryan Dalton
https://github.com/Bryandalton
