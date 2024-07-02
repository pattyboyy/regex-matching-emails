# Regex Tutorial: Matching an Email Address

In this tutorial, we'll explore a regular expression (regex) used for matching email addresses. Understanding this regex will help you validate email inputs in your applications and gain insights into the structure of regular expressions.

## Summary

The regex we'll be examining is:

```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

This regex is designed to match most common email address formats. It ensures that an email address has a username, an @ symbol, a domain name, and a top-level domain.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components

### Anchors

- `^` - The caret anchor asserts the start of the string.
- `$` - The dollar sign anchor asserts the end of the string.

These anchors ensure that the entire string matches the email pattern, not just a part of it.

### Quantifiers

- `+` - Used in `([a-z0-9_\.-]+)` and `([\da-z\.-]+)`, it means "one or more" of the preceding character set.
- `{2,6}` - Used in `([a-z\.]{2,6})`, it specifies that the preceding character set should occur between 2 and 6 times.

### Character Classes

- `\d` - Matches any digit (equivalent to [0-9]).
- `[a-z]` - Matches any lowercase letter from a to z.
- `[0-9]` - Matches any digit from 0 to 9.

### Grouping and Capturing

The regex uses parentheses `()` to create three capturing groups:

1. `([a-z0-9_\.-]+)` - Captures the username part of the email.
2. `([\da-z\.-]+)` - Captures the domain name.
3. `([a-z\.]{2,6})` - Captures the top-level domain.

### Bracket Expressions

- `[a-z0-9_\.-]` - Matches any lowercase letter, digit, underscore, dot, or hyphen.
- `[\da-z\.-]` - Matches any digit, lowercase letter, dot, or hyphen.
- `[a-z\.]` - Matches any lowercase letter or dot.

### Greedy and Lazy Match

This regex uses greedy matching by default. The `+` and `{2,6}` quantifiers will match as much as possible while still allowing the overall pattern to match.

## Author

This tutorial was created by Patrick Riedinger. You can find more of my work on my [GitHub profile](https://github.com/pattyboyy).
