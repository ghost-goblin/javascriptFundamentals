# Form Validation With JavaScript

##Regular Expressions (RegEx)

Allows us to check a series of characters for 'matches'. Use the [regex101 online tool](https://regex101.com/) to create test patterns.

![Form Validator](https://media3.giphy.com/media/c1Zf0R8KvtSCI/giphy.gif?cid=ecf05e478zvtncg1wts2ybxbbsg3qz09gxhcefiuxxj2xgvi&rid=giphy.gif)

## Simple Patterns
- `/pattern/` looks for the first instance
- `/pattern/g`, the `g` flag makes the search **global**
- `/pattern/gi`, the `i` flag makes the search match **case insenstive**

## Character Sets 
- `[]`, the character set
- `/[ph]attern/`, matches either a `p` or a `h` in the first position and occupies one space in the whole regular expression
- `[^p]000`, the `^` carrot excludes the `p` from the match

## Ranges
- `/[a-z]attern/g`, includes all the letters of the alphabet
- `/[a-z]attern/gi` add the `i` case insensitive flag OR use the following; `/[a-zA-Z]attern/`
- `/[0-9]attern/g`

## Repeating Characters
- `/[0-9]+/`, the `+` sign allows a match for the numbers in the range 0 to 9 for any length
- `/[0-9]{11}/`, create a match for a number 11 times
- `/[a-z]{11}/` matches an 11 letter word
- `/[a-z]{5, 8}/` matches a word between 5 and 8 characters long
- `/[a-z]{5,}/` matches anything _at least_ 5 characters long

## Metacharacters
Check out [this link](https://www.w3schools.com/jsref/jsref_obj_regexp.asp) for more metacharacters but here are the more common ones:
- `\d` match any digit character (same as [0-9])
- `\w` match any word character (a-z, A-Z, 0-9 and _'s)
- `\s` match a whitespace character (spaces, tabs, etc.)
- `\t` match a tab character only
- `d` -- matches the literal character, 'd'
- `\d`-- matches any digit character
For example; `/\d\s\w/` will produce a match for the `1 w` and the `5    p` pattern

## Special Characters
- `+` the one-or-more quantifier
- `\` the escape character
- `[]` the character set
- `[^]` the negate symbol in a character set
- `?` the zero-or-one quantifier (makes the preceding character optional) e.g. `/he?llo?/g`, the `e` and `o` is optional
- `.` any character whatsoever (except the newline character) e.g. `/car./g` will match `card` or `cart`
- `*` the 0-or-more quantifier (a bit like `+`) e.g. `/a[a-z]*/g`
- The backslash, `\` is the escape character e.g. `/abc\./g`

## Starting & Ending Patterns
- `/[a-z]{5}/gi` will still match more than 5 characters, [give it a go](https://regex101.com/)
- `/^[a-z]{5}$/gi`, the carrot symbol `^` in the beginning and the dollar sign `$` at the end will produce a match for 5 characters only

## Alternate Characters
- A single pipe `|` in regex means OR
- `/p|t/i` will match only either `p` or `t`
- `/(p|t)yre/i`, use parentheses to evaluate a part of the expression separately before moving on
- `/(crazy|pet|toy) rabbit/gi` or `/(crazy|pet|toy)? rabbit/gi`, remember everything before the `?` is optional

## How to create Regular Expressions?
```js
// store in a variable
var reg = /[a-z]/gi;
//OR
var reg2 = new RegExp(/[a-z]/, 'i');
```
