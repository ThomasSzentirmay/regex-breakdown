# Reguar Expressions Breakdown

This repo will just be a quick and helpful guide to regular expression specifically in ECAMScript, more commonly know as 'regex'. As an essential tool for text processing, regex enables developers and data analysts to effectively search, extract, and manipulate information within strings.

This repository serves as a quick and helpful resource to explain the idea in simple steps.

## Summary

The regex I will be using as an example for my explanation will be the following: ^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$

The above regex can be matched with a URL, which is kind of given away by the 'https' at the beginning of the expression. An example URL that matches with the regex is 'https://www.example.com/path/to/resource'.

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

- '^': The carrot symbol represents the start of a line
- '$': The dollar sign represents the end of a line

### Quantifiers

- '?': The question mark indicates that the preceding element is optional, matching 0 or 1 occurance
- '*': The asterick indicates that the preceding element can occur zero or more times
- '+': The plus sign indicates that the preceding element must occur one or more times

### OR Operator

- '|': The vertical bar seperates two alternatives, matching either the expression on the left or the one on the right

### Character Classes

- '/d': Matches any digit character (0-9)
- '/w': Matches any word character (alpharumeric character plus underscore)
- 'a-z': Matches any lowercase letter from 'a' to 'z'
- 'A-Z': Matches any uppercase letter from 'A-Z'
- '\.': Escaped dot matches a literal dot character

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
