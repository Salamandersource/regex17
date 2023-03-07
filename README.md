# Matthew Salamander's Regex Guide

## Summary

A Hex Value is a code used in design to represent colors. It's based on a numbering system with 16 possible symbols, ranging from 0 to 9 and A to F. This system is called hexadecimal, and it's useful because it can represent large numbers with fewer digits.

In HTML and CSS, a regular expression (regex) is used to match any Hex Value. The regex is as follows:

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

Let's break it down:

/^ and $/: These are anchors, which match the beginning and end of a string, respectively. In this case, they ensure that the regex matches the entire string, not just part of it.

#?: The question mark is a quantifier, which means it matches the preceding character (in this case, the hashtag) zero or one times. This allows the regex to match both six-character and three-character Hex Values, which may or may not include a hashtag at the beginning.

([a-f0-9]{6}|[a-f0-9]{3}): This is a grouping construct, which contains two subexpressions separated by the vertical bar (|), which means "or." The first subexpression matches any string of six characters that are either numbers or letters A to F. The second subexpression matches any string of three characters that are either numbers or letters A to F.

So, in summary, the regex matches any Hex Value, whether it's in the six-character or three-character format, with or without a hashtag at the beginning.

## Table of Contents

- [Literals](#literals)
- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [The OR Operator](#the-or-operator)
- [Recap](#recap)

## Regex Components

A regular expression (regex) is a pattern used to search for and match specific strings of characters. When constructing a regex pattern, there are several components you can use to make it more dynamic and flexible.

Here are some of the main components:

## Literals:

The / character is used to define a regex pattern as a literal, meaning it encompasses all possible components used to define the pattern, making it more dynamic than a method that's limited to direct matches.

## Anchors:

These components don't match specific characters; instead, they match a position before, after, or between characters in the string. The ^ and $ anchors, for example, indicate the beginning and end of a string, respectively.

## Quantifiers:

These components determine the limits of the string within your regex. They identify the least and most amount of characters your regex is searching for. The ? quantifier matches the preceding character zero or one time, while the {} quantifier sets limits for a match based on a specific number of repetitions.

## Grouping Constructs:

As a regex becomes more complex, grouping constructs are used to group different sections and indicate how they meet different requirements. These are symbolized by parentheses (()).

## Bracket Expressions:

These components include a range of characters the regex aims to match or affirm, and are enclosed in square brackets ([]).

## OR Operator:

This character (|) indicates that your regex can match the pattern on one side of the operator OR the other.

Putting these components together, you can create a regex pattern to match specific strings of characters. For example, /^#?([a-f0-9]{6}|[a-f0-9]{3})$/ is a regex pattern that matches a Hex Value (e.g., #ffffff or #fff) by using a combination of literals, anchors, quantifiers, grouping constructs, bracket expressions, and the OR operator.
