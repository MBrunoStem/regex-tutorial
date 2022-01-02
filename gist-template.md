# Regex Tutorial: Match an Email

This repository is quick rundown of some basic concepts of regex, and we'll be using the "Macthing an Email" regex as an example.


## Summary
As stated above this repository will describe the regex for "Matching an Email" or:

```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

I will explain the relevant Regex Components such as Anchors, Qualifiers, Grouping Constructs, Bracket Expressions, Character Classes, The OR Operator, Flags, and Character Escapes. Below is a Table of Contents linking to the corresponding section.


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

### Anchors
The basic Anchors used in this regex are denoted by the "^" and "dollar sign" characters repectivlely. On it's own "^" is used at the beginning of a string to match strings, whereas "dollar sign" is used at the end of a string to match strings. When "^" is at the beginning of a string and "dollar sign" is simultaneously at the end, then it will only find strings that match the entire string between our two anchors. Furthermore, our Anchors work with our Flags for our searches to only match with things that match the entirety of our regex's parameters.


### Quantifiers
The first Quantifier we see in our regex is denoted by the "+' character which appear twice in our regex. This denotes that one or more of any given class or parameters are expected after the string or parameters that preceded the "+" character.

The second Quantifier present in our regex appears towards the end in the third is denoted by the "{}" characters:

```
[a-z\.]{2,6}
```
The Bracket Expression that precedes the Quantifier is searching for any letter a-z or periods, and the Quantifier is stating that it's searching for no less than 2 but no more than 6 characters that match the criteria of the Bracket Expression.


### Grouping Constructs
The Grouping Constructs present in our regex are denoted by the "()" characters, and are useful for extracting information from a string or data. We have three different Grouping Constructs present in our regex:

```
([a-z0-9_\.-]+)
```
These set up the parameters of what's expected before the "@" in the email address. It will accept any letter a to z, any number 0 to 9, underscores, periods, and dashes.
```
([\da-z\.-]+)
```
These set up the parameters of what's expected after the "@" in the email address, but before the "." in the email. It will accept any digit, any letter a to z, periods, and dashes.
```
([a-z\.]{2,6})
```
These set up the parameters of what's expected after the "." in the email address. It will accept any letter a to z or periods, and the Quantifier at the end ensures there will be 2 to 6 characters in this group.


### Bracket Expressions
The Bracket Expressions are denoted by the "[]" characters, as the name implies. The regex will search for any characters in a string that matches the parameters defined within the Bracket Expression, and we have three Bracket Expressions present in our regex:

```
[a-z0-9_\.-]
```
This Bracket Expression will match with any string that contains any letter a to z, any number 0 to 9, underscores, periods, or hyphens.
```
[\da-z\.-]
```
This Bracket Expression will match with any string that contains any digit, any letter a to z, periods, and hyphens.
```
[a-z\.]
```
This Bracket Expression will match with any string that contains any letter a to z and periods.


### Character Classes
The only Character Class we have present in our regex is denoted by "\d", and can be found in the second Grouping Construct:

```
[\da-z\.-]
```
This character class will search for any character that is a "digit".


### The OR Operator
There are two OR Operators contained within our second and third Grouping Constructs via the Bracket Expressions.

```
@([\da-z\.-]+)
```
This OR Operator is searching for an "@" followed by any digit, any letter a to z, periods, and hyphens.
```
\.([a-z\.]{2,6})
```
This OR Operator is searching for a "." followed by 2 to 6 characters which can either be any letter a to z or a period.


### Flags
The Flags of our regex are denoted by the "/" at the beginning an end of our regex. The Flags work with our Anchors to ensure that our searches matches all of our parameters set within the Flags by the Grouping Constructs, Bracket Expressions, Quantifiers, and Character Classes.


### Character Escapes
There is one uniqe Character Escape present in our regex, but it appears a total of three times in our regex.

```
\.
```
This Character Escapes makes our regex search for a literal "." character. Whithout the backslash before the period our regex would instead search for any character except line breaks. 

## Author
Mario Bruno
* [GitHub](https://github.com/MBrunoStem)
* mbrunostem@gmail.com