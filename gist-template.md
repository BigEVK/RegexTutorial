# REGEX Tutorial for Verifying E-mail Addresses 
Do you need to verify that a phone number has been entered properly? Are you requiring someone verify their email address? How do you require these to be entered in the format you need? Enter the regex. Regular expressions, regex, can be used for just that, and so much more. Below we will be diving onto one such regex expression and break down it's components.

<!-- Introductory paragraph (replace this with your text) -->

## Summary

### This walkthrough will be focusing on requirements for an e-mail address. With the vast number of e-mail adress usernames, and varying lengths, characters within the address, and combination of letters and numbers, there is a lot to look out for. And it doesn't stop there. All e-mails must include an @ ("at" sign), followed by a domain name. 
### Domains can contain the name of the business, organization, internet service provider, custom name, or a whole mix of different characters. Lastly, we have the top-level domain. This has also grown over the years to include .com, .edu, .gov, .net, .design, .realtor, .tv, .courses, and so on.
### Let's walk through how we can use regex to veryify that we have a valid e-mail address by providing the necessary character set in our regex search algorithm.

## /^([a-z0-9_\.-]+)@([\da-z\.-]+)\\.([a-z\.]{2,6})$/

### This may look as if someone just leaned on the keyboard, but it is actually the regex sequence of characters one would use in order to verify the e-mail address is in the proper configuration.

## Below we will break down the components of this regex expression.
### Username: ([a-z0-9_\.-]+)
- matches a character in the range of "a" to "z"
- matches a character in the range of "0" to "9"
- matches an "_" character
- matches a "." character
- matches a "-" character
- quantifier "+" represents that the preceeding token must match one or more of the characters entered
### Capturing Group One is followed by an '@'
- must match an '@' character
### Domain: ([\da-z\.-]+)
- matches any digit character (0-9)
- matches a character in the range of "a" to "z"
- matches a "." character
- matches a "-" character
- quantifier "+" represents that the preceeding token must match one or more of the characters entered
### Capturing Group Two is followed by a '\\.'
- an escapred character. matches a "." character
### Top-level domain: ([a-z\.]{2,6})$
- matches a character in the range of "a" to "z"
- an escapred character. matches a "." character
- quantifier, must match between 2 and 6 of the preceeding tokens


 <!-- Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary. -->

## Table of Contents
- [Tokens](#tokens)
- [Anchors](#anchors)
- [Grouping and Capturing](#grouping-and-capturing)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)


## Regex Components

### Tokens
- Each elements used to create a regex expression is called a token. Tokens set the parameters for the expression and tell it what to look out for.

### Anchors
- Anchors, ^, $, \b, and \B, are used to signify several different components of the expression
- '^' Refered to as a 'caret', this character is used to match only from the beggining of a line. It matches a position, not a character. 
- '$' Called the 'dollar' sign, is used to match on at the end of the line, also matching only a postion, not a character. 
- Other anchors, such a \b and \B, are word and not word boundries, respectively. We do not utilize these in this case.

### Grouping and Capturing

- '()' Parenthesis are used to indicate a group that can be used later in the expression.
- In our e-mail example, we have three groups. 
- The parameters for the trhee groups are in order as follows::
    1. Username ([a-z0-9_\.-]+)
    2. Domain name ([\da-z\.-]+)
    3. Top-level domain ([a-z\.]{2,6})

### Quantifiers
- Indicate the number of times the preceding token must be matched. Quantifiers will automatically match as many occurences as possible, so setting them for specific limits is useful.
    1. '+' will match the preceeding token 1 or more times
    2. '*' will match the preceeding token 0 (zero) or more times
    3. '?' will match the preceeding token 0 or 1 time, making that character optional
    4. '{}' matches specifically the quantity of the previous token.
        + {2,4} will match from 2 to 4
        + {5} will match only 5
        + {4,} will match 4 or more


### Character Classes 
- Definea a set of characters
    + '.' matches any character except line breaks
    + '\d' matches any digit character. This is the equivilent of the bracket expression [0-9]
    + '\D' matches any character that is not a digit character. This is the equivilent of the bracket expression [^0-9]
    + '\w' matches any word character, alphanumberic and underscore, with the exception of accented or non-roman characters
    + '\W' matches any word character that is NOT alphanumeric or underscore

### Flags
- Flags are placed after the closing slash, and define additional functionality or limits. Three most common flags are:
    - i - makes the match case sensitive
    - g - makes the match global
    - m - makes the match work in multiline mode


### Bracket Expressions
- Define and match a character from a specific set. There are both predefined as well as custom sets
    + '[EAG]' will match any character in the set
    + '[^EAG]' adding a 'caret' within the brackets will "negate" the set, and match any character that is NOT in the set
    + '[P-U]' matches the range of character within the set

### Greedy and Lazy Match
- Quantifiers are inherently greedy by deflaut, and will match as many characters as possible
    - '?' will make the preceeding quantifier lazy, matching as few characters as possible


## Author

Eric is an aspiring programmer working toward his Bachelor's degree in Computer Science. He has been wokring with computers most of his life and now diving into how to make them function for maximum benefit. You can see some of the projects he is working at his github page. 
https://github.com/BigEVK