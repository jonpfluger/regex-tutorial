# Regex Tutorial

Regex is short for regular expression. A regex is a sequence of characters that defines a specific search pattern. They are used to find certain patterns within a string. They can also be used to replace those characters or a sequence of them. Regular expressions can be included in code or search algorithms. They are often used to validate input.

## Summary

In this example, we will be looking at the following regular expression which would be used to validate an email address:

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

Each component of this regex has a unique responsibility to make sure that a user enters an email address that begins with an unspecified number of characters preceding the @ symbol, followed by a domain.


## Table of Contents

- [Anchors](#anchors)
- [Bracket Expressions](#bracket-expressions)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Character Escapes](#character-escapes)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Author](#author)
- [Sources](#sources)

## Regex Components

A regex is considered a literal, so the pattern must be wrapped in slash characters (/). Let's take a look at the components of a regex.

### Anchors

The characters `^` and `$` are both anchors, but each has its own uses. 

The `^` anchor means to look for a string that begins with the characters that follow it. The characters that follow can be specific, such as "cat" or "the cat", or you can use bracket expressions to find a range of possible matches. We will look at Bracket Expressions in more detail later.

The `$` anchor means to look for a string that ends with the characters that precede it. The preceding characters behave the same way as the other anchor, where you can be specific or include bracket expressions.

### Bracket Expressions

Bracket expressions `[]` are used to search for a range of characters. They are sometimes referred to as a "positive character group".

Let's look at our email example again: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

The first bracket is looking for a string that may include any lowercase letter a-z, and/or may include any number 0-9, and/or may include the characters `_\.-` 

### Quantifiers

Quantifiers are used to set limits of the string were searching for. It is often used to set the minimum and maximum number of characters. In our email example, towards the end of it, we see `{2,6}`. That quantifier is setting the min max parameters onto the bracket expression that precedes it.

### Grouping Constructs

Grouping constructs `()` allow us to check multiple parts of a string. Each section inside parentheses is called a subexpression.

In our email example, `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`, we have three subexpressions separated by the specific characters `@` and `.`

### Character Escapes

The blackslash `\` in a regex escapes a character that would otherwise be interpreted literally. If we look back at the email example, we see `\.` being used to escape the period character.

### Character Classes

A character class defines a set of characters.
- `.` Matches any character except the newline character (\n)
- `\d` Matches any Arabic numerical digit. Equivalent to `[0-9]`
- `\w` Matches any alphanumeric character from the basic Latin alphabet, including the underscore (_). Equivalent to `[A-Za-z0-9_]`
- `\s` Matches a single whitespace character, including tabs and line breaks

In our email example `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`, we see that the second bracket expression contains the character class `\d`, which is used instead of `[0-9]`.

### Flags

Earlier we said that because a regex is a literal, it must be wrapped in slash characters. Flags are the one exception to this rule. They are placed after the final slash.
- `g` Global search: test against all possible matches in a string.
- `i` Case-insensitive search: case should be ignored while attempting a match in a string
- `m` Multi-line search: a multi-line input string should be treated as multiple lines

## Author

This gist was written by Jon Pfluger, a full-stack bootcamp student excited to start his career in tech! When Jon is not coding, he likes to play guitar. In addition, Jon is also a gamer, which helped cultivate an interest in technology from a young age.

Github: https://github.com/jonpfluger

#### Sources
- https://coding-boot-camp.github.io/full-stack/computer-science/regex-tutorial
- https://www.regexpal.com/?fam=104026