# Regex Tutorial: Matching an Email

This tutorial is going to explain the use of regex to match an email using the expression /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/. This can be useful when validating emails that can  be using applications and technologies such as Node or MongoDB.

## Summary

A regular expression is a sequence of characters that defines a search pattern.  It is commonly used to find patterns within a string.  It can also be used to find and replace characters within a string or validate its input.  This tutorial will walk through the components of a regex and how iti related to matching an email.

Regex Pattern : /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

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

Anchors are special characters that allow you to match positions within a string rather than matching specific characters. They are used to define the start or end of a line, word, or input string. Anchors do not consume any characters themselves, but they determine the position where a match should occur. 
The anchors used in this regex expression for matching an email are ^ (caret) , which indicates the beginning of the string and $ (dollar sign) to indicate the ending of the string.

### Quantifiers

Quantifiers are special characters or symbols that specify the number of occurrences a pattern or character should match. They allow you to define the quantity or repetition of a particular element within a regex pattern. Quantifiers can be applied to individual characters, groups of characters, or even other regex metacharacters. Quantifiers in this regex includes the + operator, which will connect the username + email service + .com. Another quantifier for this regex includes {2,6}, which will allow a match range of 2-6 characters for the character set of [a-z\.].

### Grouping Constructs

Grouping constructs are components that are marked with an parenthesis.  Grouping constructs can also be known as subexpressions.  Capturing group one in this expression is ([a-z0-9_\.-]+) that matches the user email name. The second capturing group is ([\da-z\.-]+) which will match the email service. Then lastly, the third group is ([a-z\.]{2,6}) to capture the .com end of the email.

### Bracket Expressions

Bracket expressions, also known as character classes, are a way to specify a set of characters that you want to match. They allow you to define a range or a set of characters that a single position in the regex pattern can match. Bracket expressions provide a convenient way to match a specific set or range of characters in a regex pattern. They offer flexibility and precision in defining character matches within a regular expression.  

The first part of the expression [a-z0-9_\.-] shows that it could be a lowercase letter from a-z, any digit 0 through 9, and could be the remaining characters of "_", "-", and ".". 

The second part of the expression [\da-z\.-] shows that it can be a single digit 0-9, any character a-z (case senstive), and the remainging characters of "." and "-".

The third part of the expression [a-z\.] matches any charactret a-z(case senstive) and the character ".". 

### Character Classes

Character classes are components that define a set of characters. There is one character class in this regex. The character class in this expression is \d, which matches a single characters that is a digit from 0-9. It will only match a single digit such as "2", but not "22".

### The OR Operator

the OR operator allows you to specify alternatives for a pattern match. It allows you to match one pattern or another pattern at a specific position in the input string. The OR operator is represented by the vertical bar character (|).  The OR operator is useful when you want to match different variations of a pattern or when you have multiple alternatives to consider at a specific position in the input string. It provides flexibility in defining patterns that can match multiple options.  It is not directly used in this regex.

### Flags

Flags are optional parameters that modify the behavior of the regex pattern matching. They are represented by single characters or symbols placed after the closing delimiter of the regex pattern (usually a forward slash "/") or embedded within the pattern itself. Flags provide additional control and customization options when working with regex patterns. They modify how the patterns are matched and influence the behavior of the regex engine. By using flags, you can fine-tune the matching process to suit your specific requirements.

### Character Escapes
 
Character escapes are special sequences that represent a specific character or a set of characters. They are used to match characters that have special meanings in regex or to match characters that are difficult to type or represent directly. Character escapes are essential for matching special characters, representing characters with special meanings, or working with Unicode characters in regex. They ensure that specific characters are interpreted literally and not treated as metacharacters or special sequences.

## Author

The author for this tutorial is Kar Sodhi. For more information visit my github profile (https://github.com/karsodhi)
