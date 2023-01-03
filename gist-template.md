# Regex Tutorial

A regex, which is short for regular expression, is a sequence of characters that defines a specific search pattern. When included in code or search algorithms, regular expressions can be used to find certain patterns of characters within a string, or to find and replace a character or sequence of characters within a string. They are also frequently used to validate input.

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



### Bracket Expressions



### Quantifiers



### Grouping Constructs



### Character Escapes



### Character Classes



### Flags



## Author

This gist was written by Jon Pfluger, a full-stack bootcamp student excited to start his career in tech! When Jon is not coding, he likes to play guitar. In addition, Jon is also a gamer, which helped cultivate an interest in technology from a young age.

Github: https://github.com/jonpfluger

#### Sources
- https://coding-boot-camp.github.io/full-stack/computer-science/regex-tutorial
- https://www.regexpal.com/?fam=104026