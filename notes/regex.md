# Regular Expressions in Python

# Glob != regular expression

Type strings to match items exactly

Special characters:
	. ^ $ * ? [ ] { } \\ | ( )

. -- Full stop - matches any single character except newline character ("\n")
	- same as ? in linux/glob
? -- matches 1 or zero characters
	- ex: r"e?"
* -- Kleene star - give me zero or any number of the character
	- ex: "hello\*" -- hellooooooo
+ -- Plus sign - char should appear 1 or more times 
[ ] -- any of these characters might match
	- ex: r"[hH]ello"
	- ex: [a-zA-Z0-9] means match anything in this custom range
	- so [lmnop] is equivalent to [l-p]


\w -- matches any "word" character, i.e. [a-zA-Z0-9_]
\W -- matches anything NOT a word character
\s -- matches any whitespace character, i.e. [\t\n \r]
\S -- matches any non-whitespace character
	- note: does not include full stop
\d -- matches any numeric value

^ -- when used in a character class, negates it
	- ex: ^\s = \S
	- otherwise, means the start of a string
$ -- matches the end of a string

Range brackets:
{x} -- match the previous character x times
	- ex: r"\w{3}" = r"\w\w\w"
{x,y} -- match the previous character from x to y times (inclusive)
{x, } -- match the previous character at least x times
{ ,y} -- match the previous character at most y times

Grouping parenthesis:
() -- groups a list of regex expressions


