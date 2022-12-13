# Reggie-My-Ex

In this gist we will exploring the idea of a regex.  We will talk about what a regex is in general and look at a specific example and the individual components that allow it to function as intended.  A regex is a sequence of characters that defines a specific search pattern.  A search pattern will allow a user to search through a group of characters like a document or a group of code and fid the characters that match the specified parameters.

## Summary

  A hex value is positional numbering system that allow us to represent large numbers in a more concise way than traditional binary numbering.  This allows for user to distinguish the numbers more easily as we will use a string of numbers and letters. The below regex matches a hex value.
`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [OR Operator](#or-operator)



## Regex Components

### Anchors
`“^”` is an anchor which signifies that this in the beginning of the statement or line of text.   This means that the expression we are looking to match will begin with the following character `“#”` this is a very common way to start a hex value when the value is meant to represent a color

The other anchor we will see is the ending anchor.
The search is wrapped in the closing parenthesis and then followed by a dollar sign `“$”` but why?
`“$”` does not mean we have to pay for the search! It means this is the end the statement.  This is how we close a regex search.  And that is how the regex for matching a hex value works!  If we wanted to search for a specific hex value, we could limit the characters we ask the regex to search for but this is used to search for hex values in general and can be tailored by the user for their purposes.


### Quantifiers
Often a hex value will begin with a hash. However, it’s not required in all cases that the hex value beings with the hash symbol.  Therefore, the question mark symbol `“?”` follows the hash.  The question mark character “?” makes the preceding character optional within the search.

### Grouping and Capturing

The second part of the hex value expression is wrapped in parenthesis “()” and we will break this section down further.  However, its important to understand that everything contained inside the parentheses is interpreted as a group of characters and not handled individually.  So in that sense this is the final segment of this expression.

### Bracket Expressions
Let’s explore what’s inside the parentheses here.
First, we have square brackets `“[]”` which means that the characters inside these brackets should match any one character in the string.  So, we have `[a-f0-9]` and this means that our search will find any string that contains “a,b,c,d,e or f” and “0,1,2,3,4,5,6,7,8 or 9” this is incredibly powerful.  This is a result of the characters being separated by the hyphen which is not read as a character but is apart of the bracket expression syntax.  We can see that immediately following the square brackets we have curly braces `“{}”` with a number inside `{6}`.  This part of the expression is a meant to limit the quantity of characters in the search.  So, since we are looking for characters a-f and 0-9 we are also limiting the search to match a string of 6 characters.  


### OR Operator
Next, we are met with the bar character `“|”` which signifies “or” meaning that the search can match the previous parameters OR the following parameters.  In our regex we have a repetition of the possible characters being included from our previous section `[a-f0-9]` however this time the quantity limiter is listed as 3 characters by using `“{3}”`.





## Author


This gist was written by Timothy Barnaby.  I am a full stack web developer with a background in natural human language education and acquisition.  For more information about my work checkout my [tbarns](https://github.com/tbarns).

Send me an email at  [tbarnaby1@gmail.com](mailto:tbarnaby1@gmail.com) if you would like to get in contact about working together in the future or have any questions. 