# REGEX Tutorial for Verifying E-mail AddressesTitle 
Do you need to verify that a phone number has been entered properly? Are you requiring someone verify their email address? How do you require these to be entered in the format you need? Enter the regex. Regular expressions, regex, can be used for just that, and so much more. Below we will be diving onto one such regex expression and break down it's components.

<!-- Introductory paragraph (replace this with your text) -->

## Summary

### This walkthrough will be focusing on requirements for an e-mail address. With the vast number of e-mail adress usernames, and varying lengths, characters with the address, and combination of letters and numbers, there is a lot to look out for. And it doesn't stop there. all e-mails must include an @ ("at" sign), followed by a domain name. 
### Domains can contain the name of the business, organization, internet service provider, custom name, or a whole mix of different characters. Lastly, we have the top-level domain. This has also grown over the years to include .com, .edu, .gov, .net, .design, .realtor, .tv, .courses, and so on.
### Let's walk through how we can use regex to veryify that we have a valid e-mail address by providing the necessary character set in our regex search algorithm.

## /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

### This may look as if someone just leaned on the keyboard, but it is actually the regex sequence of characters one would use in order to verify the e-mail address is in the proper configuration.

### Below we will break downn the components of the regex expression.

 <!-- Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary. -->

## Table of Contents

- [Anchors](#anchors)
- [Grouping and Capturing](#grouping-and-capturing)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)

- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors
- Anchors, ^, $, \b, and \B, are used to signify several different components of the expression
- '^' Refered to as a 'caret', this character is used to match only from the beggining of a line. It matches a position, not a character. 
- '$' Called the 'dollar' sign, is used to match on at the end of the line, also matching only a postion, not a character. 
- Other anchors, such a \b and \B, are word and not word boundries, respectively. We do not utilize these in this case.

### Grouping and Capturing
- '()' Parenthesis are used to group that can be used later in the expression.

### Quantifiers

### OR Operator

### Character Classes

### Flags
- i - makes the match case sensitive
- g - makes the match global
- m - makes the match work in multiline mode



### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)