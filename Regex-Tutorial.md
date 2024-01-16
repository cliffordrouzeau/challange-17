# Regex in depth tutortial 

This document will go in depth about Regax and all its parts, today we will go over Anchors, Quantifiers, grouping constructs, bracket expression, character classes, the OR operator, flags, and character escapes to further your understanding of regax.

## Summary

A regular expression, sometimes referred to as rational expression, is a sequence of characters that specifies a match pattern in text. Usually such patterns are used by string-searching algorithms for "find" or "find and replace" operations on strings, or for input validation. This would be an example of regex [a-zA-Z0-9_] and we will get more in dept about what this means part by part.

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

Regexes are composed of several different components that work together to define a search pattern. The most common components include anchors, character classes, quantifiers, and alternation. Square brackets [ ] — means exactly one character, and A regex is considered a literal, so the pattern must be wrapped in slash characters (/).

### Anchors

Anchors provide a way to limit how a regex matches a particular string by telling the regex engine where matches can begin and where they can end. Anchors are a bit strange in the world of regex, they don't match any characters, What they do is ensure that a regex matches a string at a specific place whether the beginning or end of the string or end of a line, or on a word or non-word boundary. The two characters used are ^ and $. ^ matches the start of a line and anchors a literal at the beginning of that line and $ matches the end of a line and anchors a literal at the end of that line.

### Quantifiers

Quantifiers denote how many times a character, a character class, or group should appear in the target text for a match to occur. + will match any character it is appended to if the character appears at least once, * is similar to the + character but with a slight difference. When you append * to a character, it means you want to match any number of that character including none, ? implies "optional". When you append it to a character, it means the character may or may not appear. {N}, when appended to a character or character class, specifies how many of the character we want. For example /\d{3}/ means match three consecutive digits. {N,M} is called the interval quantifier and is used to specify a range for the minimum and maximum possible match. For example /\d{3, 6}/ means match a minimum of 3 and a maximum of 6 consecutive digits.{N, } denotes an open-ended range. For example /\d{3, }/ means match any 3 or more consecutive digits.

### Grouping Constructs

What if you want to use a quantifier like + or * on more than one character at a time – say a character class or group? You can group them together as a whole using the parentheses before appending the quantifier, for example the regex code /abc+(xyz+)+/i, The first + matches the c of abc, the second + matches the z of xyz, and the third + matches the subexpression xyz, which will match if the sequence repeats

### Bracket Expressions

Brackets indicate a set of characters to match. Any individual character between the brackets will match, and you can also use a hyphen to define a set, You can use the ^ metacharacter to negate what is between the brackets. You will often see ranges of the alphabet or all numerals. [A-Za-z] [0-9] Remember that these character sets are case sensitive, unless you set the i flag.

### Character Classes

A character class is used to match any one of several characters in a particular position. To denote a character class, you use square brackets [] and then list the characters you want to match inside the brackets. so it you had /clif[fo]ord/ it would find a word that starts with clif then matches a f or an o between clif and ord.

### The OR Operator

Grouping and alternation are core features of every modern regular expression library. You can provide as many terms as desired, as long as they are separated with the pipe character: |. This character separates terms contained within each (...) group. For example ^I like (cats|rats), but not (dogs|lions).$ this will match back 4 possibilitys 

I like cats, but not dogs.
I like cats, but not lions.
I like rats, but not dogs.
I like rats, but not lions.

### Flags

Flags or modifiers are characters that enable advanced search features including case-insensitive and global searching. You can use them individually or collectively, some include, g is used for global search which means the search will not return after the first match, i is used for case-insensitive search meaning that a match can occur regardless of the casing, m is used for multiline search, and u is used for Unicode search.

### Character Escapes

A metacharacter has to be escaped with a backslash if you want it to appear as a literal in your regular expression. By escaping a metacharacter in regex, the metacharacter loses its special , If you need to use any of the special characters literally (actually searching for a "*", for instance), you must escape it by putting a backslash in front of it. For instance, to search for "a" followed by "*" followed by "b", you'd use /a\*b/ — the backslash "escapes" the "*", making it literal instead of special

## Author

You have made it through the tutorial I hope I have helped you understand regex more then before, my whole goal is to help people further their education and work towards their goals, personally I am a hard-working and driven individual who isn't afraid to face a challenge and neither should you. I'm passionate about my work and I know how to get the job done from countless hours of research and learning out to solve every problem i come across, even now im taking a bootcamp corse to further my knowledge about full stack development to widen my horizon in my work fields. I hope this tutorial helped and here is a link to my [github](https://github.com/cliffordrouzeau) with many more projects and information. 
