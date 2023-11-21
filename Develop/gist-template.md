Regex GistOfIt

Hello, my name is Reiken Stuart. I am a coding student at the U of U. I will be attempting to create a tutorial for Regex search pattern.

## Summary

We will go through each of the components of the regular expression below and examine each component of this regex to see how it plays a vital role for the user to enter a valid email address. Hope this will be helpful for those who indulge.

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

/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/

Slashes /.../ are meant for creating a regex using a regex literal. They have the sames role as quotes for strings. That means first slash defines introducing regex literals and last one at the end closes the expression.

### Anchors

The caret ^ anchor indicates the beginning of the string. The dollar $ anchor indicates the end of the string. In our given regex ^ is on the start and $ is in the end: /^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/. An exact string match, such as ^The, where the strings "The" or "The person" match, but "the" and "the person" do not. This is because a regex is case-sensitive.

### Quantifiers

Quantifiers set the limits of the string that your regex matches. They frequently include the minimum and maximum number of characters that your regex is looking for. Quantifiers specify how many instances of a character, group, or character class must be present in the input for a match to be found. Our regex has two quantifiers: + and {}. The plus + matches any string that contains at least one or more expression on its left. In our regex, it matches any string that contains one or more expressions on its left enclosed in square brackets []. Each of these quantifiers can be made lazy by adding the ? symbol after it, meaning it will match as few occurrences as possible.

Quantifiers match as many occurrences of particular patterns as possible. They include the following:

*—Matches the pattern zero or more times

+—Matches the pattern one or more times

?—Matches the pattern zero or one time

{}—Curly brackets can provide three different ways to set limits for a match:

{ n }—Matches the pattern exactly n number of times

{ n, }—Matches the pattern at least n number of times

{ n, x }—Matches the pattern from a minimum of n number of times to a maximum of x number of times

### Grouping Constructs

Grouping constructs delineate the subexpressions of a regular expression and capture the substrings of an input string. The primary way you group a section of a regex is by using parentheses (()). Each section within parentheses is known as a subexpression. Other ways we can construct grouping are:

Match a subexpression that is repeated in the input string.

Apply a quantifier to a subexpression that has multiple regular expression language elements. For more information about quantifiers, see Quantifiers.

Include a subexpression in the string that is returned by the Regex.Replace and Match.Result methods.

Retrieve individual subexpressions from the Match.Groups property and process them separately from the matched text as a whole.

### Bracket Expressions

Anything inside a set of square brackets ([]) represents a range of characters that we want to match. These patterns are known as bracket expressions. Each set of brackets can have any number of characters that it can be matched to and this is done by settings ranges of characters that include letters, numbers, and special characters. There are a few ways that we can break down bracket expressions, such as:

[a-z]—The string can contain any lowercase letter between a–z. Keep in mind that this looks for lowercase characters only.

[0-9]—The string can contain any number between 0–9

[_-]—The string can contain an underscore or hyphen.

[a-zA-Z] The string can contain uppercase from A-Z so long as we change to this expression.

### Character Classes

A character class in a regex defines a set of characters, any one of which can occur in an input string to succesfully complete a match. 

Here are some of the other common character classes:

.—Matches any character except the newline character (\n)

\d—Matches any Arabic numeral digit. This class is equivalent to the bracket expression [0-9].

\w—Matches any alphanumeric character from the basic Latin alphabet, including the underscore (_). This class is equivalent to the bracket expression [A-Za-z0-9_].

\s—Matches a single whitespace character, including tabs and line breaks

### The OR Operator

Using the OR operator (|), the expression [abc] could be written as (a|b|c). This means that [a-z0-9_-] searches for alphanumeric characters or the two special characters included in the pattern. Often, we want to add this same logic outside of a bracket expression, in most cases using it within a grouping construct or between two different grouping constructs. An example of this would be as follows:

Before OR operator: (abc):(xyz) After OR operator: (a|b|c):(x|y|z)

### Flags

Flags are placed at the end of a regex, after the second slash, and they define additional functionality or limits for the regex. However this RegEx flag is not a part of the email code either. This is purely informational in relation to the original purpose of this tutorial.

The three Flags that you are most likely to see regularly are:

g which is global = matching ALL the possibilities in the string that will yield a match. Matching the beginning and end of the string. Doesn't return after initial match and starts again searching from the end of the pervious match.

m which is multiline = line-by-line search versus searching through the string in its entirety.

i which is case-insensitive = prevents capital letters and lowercase letter from stopping a match, and relates directly to case sensitivity.Would look like /XyZ/

### Character Escapes

Backslashes (\) in a regex is used as escape for a character that would otherwise be interpreted as literal. One example of this is with an open curly brace({) that is used to begin a quantifier, but if you where to add a backslash before the brace(\{) this would mean that the regex should look for an open curly brace instead to define the quantifier. This is used often when looking for strings with special characters that are the same as a specific component of a regex.

## Author

Hello, my name is Reiken Stuart. This is an my simple tutorial of regex pattern. Please, feel free to visit my Github: https://github.com/13rstuart7/regex_tutorial

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
