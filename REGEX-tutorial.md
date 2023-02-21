# Regular Expression - Tutorial: Matching a URL 


Regular expressions or **REGEX**, is a way to describe a pattern that are used to match character combinations in strings. Or validate specific string or patterns of text in a sentence, document, or any other iput.
**REGEX** can match any valid URL.


-------
## `Summary`


In this tutorial, We are going to go break down the components of **REGEX** matching a giving URL utilizing regular expressions in javascrip.

**/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/**


-------
## `Table of Contents`

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [Character Escapes](#character-escapes)


-------
## `Regex Components`


Regular expressions are builded by many components.
Note that Regular expressions must be wrapped in slash characters /.

Let's take a look to each element to understand how this works.


-------
### `Anchors`

Anchors match a position before or after other characters.

^ Matches at the beginning of the target string.

$ Matches at the end of the target string

^ $  By enclosing the REGEX between ^ and $ we are asking the search function to match exactly what is included between them.


-------
### `Quantifiers`

We use Quantifiers to define the number of timer that a given **REGEX** may be identified.
The most common quantifiers are the question mark ?, the asterisk * and the plus sign +.

? Matches the preceding pattern 0 or 1 times. For example: /h?alloween?/ matches "all" in "tall" and "en" in "happen"
* Matches the preceding pattern 0 or more times. For example: /christmas*/ matches "christmas" in "christ" and "mas" in "master", but there are no matches in "food"
+ Matches the preceding pattern 1 or more times. For example: /a+/ matches each a in "again"
{n} The preceding item is matched exactly n times.
{min,} The preceding item is matched min or more times.
{,max} The proceding item is matched up to max times.
{min,max} The preceding item is matched at least min times, but not more than max times.

> _For our example for matching URL_


**/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/**

? is used in different places: https?, \/\/)?, *)*\/?$/
* used to signify that [\/\w \.-] could match 0 or more items and ([a-z\.]{2,6})([\/\w \.-]*) could match 0 or more items
+ is used to signify that the pattern ([\da-z\.-]+) should match 1 or more item


-------
### `Grouping Constructs`

Grouping constructs delineate the subexpressions of a regular expression and capture the substrings of an input string
() Are used to define the scope and precedence of the operators
There are three grouping techniques: random, purposeful and topical

> _For our example for matching URL_

**/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/**

We use subexpressions (https?:\/\/), ([\da-z\.-]+), ([a-z\.]{2,6}), ([\/\w \.-]*)


-------
### `Bracket Expressions`

Bracket Expressions represent a range or list of character classes enclosed in brackets []
Brackets indicate a set of characters to match. Any individual character between the brackets will match, and we can use a hyphen to define a set. We can use ^metacharacter to negate what is between the brackets.
We use bracket expressions to match single characters in a list, or a range of characters in a list.

> _For our example for matching URL_

**/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/**

[\da-z\.-] this matches a single character in the range between a snd z.
[a-z\.] this matches a single character in the range between a and z with a character.
[\/\w \.-] the slash, alphanumeric, dot and hyphen will get a match


-------
### `Character Classes`

Character Classes is a set of characters enclosed within square brackets, it specifies the characters that will successfully match a single character from a given input string, you can tell the **REGEX** engine to match only one out of several characters. We can place any characters we want to match between square brackest [] if we want to match an aor an i, we use [ai]

> _For our example for matching URL_

**/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/**

([\da-z\.-]+) Matches a single character that is a digit
[\/\w \.-] Matches any word character, alphanumeric character plus underscore


-------
### `Character Escapes`

We are going to use Character Escapes when a character is NOT supoosed to be interpreted.
The backslash \ in a regular expression precedes a literal character, we can also escapecertain letters that represent common character classes, such as \w for a word character or \s for a space.

> _For our example for matching URL_

**/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/**

\d in ([\da-z\.-]+)  Matches a single character that is a digit
\w in [\/\w \.-] Matches any word character, alphanumeric character plus underscore.



-------
## `Author`

Zazil Gomez, Web Development at UW
* GitHub **https://github.com/zazgh**
