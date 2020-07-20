# Regex

```
abc…	Letters
123…	Digits
\d	Any Digit
\D	Any Non-digit character
.	Any Character
\.	Period
[abc]	Only a, b, or c
[^abc]  Not a, b, nor c
[a-z]	Characters a to z
[0-9]	Numbers 0 to 9
\w	Any Alphanumeric character
\W	Any Non-alphanumeric character
{m}	m Repetitions
{m,n}	m to n Repetitions
*	Zero or more repetitions
+	One or more repetitions
?	Optional character (0 or 1 occurrence)
\s	Any Whitespace
\S	Any Non-whitespace character
^…$	Starts and ends
(…)	Capture Group
(a(bc)) Capture Sub-group
(.*)	Capture all
(abc|def) Matches abc or def
```

The 12 special characters (need to be escaped):
the backslash \, the caret ^, the dollar sign $, the period or dot ., the vertical bar or pipe symbol |, the question mark ?, the asterisk or star *, the plus sign +, the opening parenthesis (, the closing parenthesis ), the opening square bracket \[, and the opening curly brace {

# Examples:
### 1. Quick cheat sheet

This expression | matches this | but NOT this
--- | --- | ---
a | a | b
\\\.\\\* | .* | dog
100 | 100 | ABCDEFG
.art | dart, cart, tart | art, hurt, dark
a+b | ab, aaab | b baa
a\*b | b, ab, aaab | daa
.\*cat | cat, 9393cat, the old cat,	c7sb@#puiercat | dog
a\[n\]? h | a herb, an herb | ann hat
(ab)\*c | abc, ababababc | ababab, ababd
(.a)+b | xab, ra5afab | b, aagb
\[aeiou\]\[0-9\] | a6, i3, u2 | ex, 9a, $6
\[^cfl\]og | dog, bog | cog, fog
END\[.\] | END. | END;, END DO, ENDIAN
^(the cat).+ | the cat runs | see the cat run
.+(the cat)$ | watch the cat | the cat eats


### 2. To match US phone numbers
```
let pattern = “[0–9]{3}-[0–9]{3}-[0–9]{4}”
```
