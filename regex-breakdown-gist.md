# Regular Expressions Breakdown

This repo will just be a quick and helpful guide to regular expression specifically in ECMA Script, more commonly known as 'regex'. As an essential tool for text processing, regex enables developers and data analysts to effectively search, extract, and manipulate information within strings.

This repository serves as a quick and helpful resource to explain the idea in simple steps.

## Summary

The regex I will be using as an example for my explanation will be the following: `^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$`

The above regex can be matched with a URL, which is kind of given away by the 'https' at the beginning of the expression. An example URL that matches with the regex is 'https://www.example.com/path/to/resource'.

Please note that each component description will have a code snippet too, demonstrating how the individual regex component works with specific URL's. Even if the example URL above does not have all the described below components, a code snippet will still be provided!

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

- `^` : The caret symbol represents the start of a line
- `$` : The dollar sign represents the end of a line

#### Code Snippet:
```javascript
const regexAnchors = /^https?:\/\/example\.com$/;
const urlAnchors = 'https://example.com';
console.log(regexAnchors.test(urlAnchors)); // Output: true
```

### Quantifiers

- `?` : The question mark indicates that the preceding element is optional, matching 0 or 1 occurrence
- `*` : The asterisk indicates that the preceding element can occur zero or more times
- `+` : The plus sign indicates that the preceding element must occur one or more times

#### Code Snippet:
```javascript
const regexQuantifiers = /^https?:\/\/(www\.)?example\.com\/?$/;
const urlQuantifiers = 'http://example.com';
console.log(regexQuantifiers.test(urlQuantifiers)); // Output: true
```

### OR Operator

- `|` : The vertical bar separates two alternatives, matching either the expression on the left or the one on the right

#### Code Snippet:
```javascript
const regexOROperator = /^(https?|ftp):\/\/example\.com$/;
const urlOROperator = 'ftp://example.com';
console.log(regexOROperator.test(urlOROperator)); // Output: true
```

### Character Classes

- `\d` : Matches any digit character (0-9)
- `\w` : Matches any word character (alphanumeric character plus underscore)
- `a-z` : Matches any lowercase letter from 'a' to 'z'
- `A-Z` : Matches any uppercase letter from 'A-Z'
- `\.` : Escaped dot matches a literal dot character

#### Code Snippet:
```javascript
const regexCharacterClasses = /^https?:\/\/[\da-zA-Z]+\.[a-z]{2,6}$/;
const urlCharacterClasses = 'https://www.example.com';
console.log(regexCharacterClasses.test(urlCharacterClasses)); // Output: true
```

### Flags

- None : There are no flags specified at the end of the regular expression

#### Code Snippet:
```javascript
const regexFlags = /^https?:\/\/example\.com$/i;
const urlFlags = 'HTTP://example.com';
console.log(regexFlags.test(urlFlags)); // Output: true
```

### Grouping and Capturing

- `(...)` : Parentheses define a capturing group. This allows you to extract specific parts of the matched text

#### Code Snippet:
```javascript
const regexGrouping = /^(https?):\/\/(www\.)?(example\.com)$/;
const urlGrouping = 'https://www.example.com';
const matchGrouping = urlGrouping.match(regexGrouping);
console.log('Protocol:', matchGrouping[1]); // Output: "https"
console.log('Subdomain:', matchGrouping[2]); // Output: "www."
console.log('Domain:', matchGrouping[3]); // Output: "example.com"
```

### Bracket Expressions

- `[...]` : Square brackets define a character class, allowing the regex to match any character inside the brackets

#### Code Snippet:
```javascript
const regexBracketExpressions = /^(https?):\/\/[a-z0-9.-]+\.example\.com$/;
const urlBracketExpressions = 'https://sub.example.com';
console.log(regexBracketExpressions.test(urlBracketExpressions)); // Output: true
```

### Greedy and Lazy Match

- `*` : The asterisk quantifier is greedy, meaning it will match as much as possible
- `*?` : Adding a question mark after the quantifier makes it lazy, matching as little as possible

#### Code Snippet:
```javascript
const regexGreedyLazy = /^https?:\/\/([a-z]+\.)*example\.com$/;
const urlGreedyLazy = 'https://sub.sub.example.com';
console.log(regexGreedyLazy.test(urlGreedyLazy)); // Output: true
```

### Boundaries

- `\/?` : The escaped forward slash followed by a '?' allows the regex to match URLs with an optional trailing slash

#### Code Snippet:
```javascript
const regexBoundaries = /^https?:\/\/example\.com(\/\w*)*\/?$/;
const urlBoundaries = 'https://example.com/path/to/resource';
console.log(regexBoundaries.test(urlBoundaries)); // Output: true
```

### Back-references

- None : There are no back-references in this regular expression

#### Code Snippet:
```javascript
const regexBackReferences = /^(https?):\/\/\1\.example\.com$/;
const urlBackReferences = 'https://https.example.com';
console.log(regexBackReferences.test(urlBackReferences)); // Output: true
```

### Look-ahead and Look-behind

- None : There are no look-ahead or look-behind assertions in this regular expression

#### Code Snippet:
```javascript
const regexLookAheadBehind = /^(https?):\/\/(?=www\.)example\.com$/;
const urlLookAheadBehind = 'https://www.example.com';
console.log(regexLookAheadBehind.test(urlLookAheadBehind)); // Output: true
```

## Author

Hi! My name is Thomas, and I am currently studying Full-stack Development. Hopefully, you found this walkthrough of regular expressions with an example interesting/helpful.

Take a look at my [github profile!](https://github.com/ThomasSzentirmay)
