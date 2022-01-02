# Regex Tutorial

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
The basic Anchors used in this regex are denoted by the "^" and "dollar sign" characters repectivlely. On it's own "^" is used at the beginning of a string to match strings, whereas "dollar sign" is used at the end of a string to match strings. However, such as in the "Match an Email" regex, when "^" is at the beginning and "dollar sign" is simultaneously at the end, then it will only find strings that match all of the parameters present between the two anchors.

### Quantifiers
The first Quantifier we see in pour regex is denoted by the "+' character. This denotes that one or more of any given class or parameters are expected after the parameters that preceded the "+" character.

The second Quantifier present in our regex appears towards the end in the third is denoted by the "{}" characters:

```
{2,6}
```
Meaning that this regex is searching for no less than two but no more than six characters that match the parameters that preceded the Quantifier:

```
[a-z\.]{2,6}
```

### Grouping Constructs
The Grouping Constructs present in our regex are denoted by the "()" characters, and are useful for extracting information from a string or data. We have three different Grouping Constructs present in our regex:

```
([a-z0-9_\.-]+)
```
These set up the parameters of what's expected before the "@" in the email address.
```
([\da-z\.-]+)
```
These set up the parameters of what's expected after the "@" in the email address, but before the "." in the email.
```
([a-z\.]{2,6})
```
These set up the parameters of what's expected after the "." in the email address.

### Bracket Expressions


### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author
Mario Bruno
* [GitHub](https://github.com/MBrunoStem)
* mbrunostem@gmail.com