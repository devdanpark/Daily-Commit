# String Object
## Control Characters
- indexOf(substr, [,start]) :Returns the position of the first found occurrence of a specified value in a string

- lastIndexOf(substr, [,start]) : Returns the position of the last found occurrence of a specified value in a string

- startWith(search [,pos]): Checks whether a string begins with specified characters

- endWith(search[,pos]): Checks whether a string ends with specified string/characters

- includes(search [,pos]): Checks whether a string contains the specified string/characters

- charAt(n): Returns the character at the specified index (position)

- slice(start [,end]): Extracts a part of a string and returns a new string

- substring(start [,end]): Extracts the characters from a string, between two specified indices

- substr(start [,cnt]): Extracts the characters from a string, beginning at a specified start position, and through the specified number of character

- split(str [,limit]): Splits a string into an array of substrings

### Regular Expression
- match(reg): Searches a string for a match against a regular expression, and returns the matches
- replace(reg, rep): Searches a string for a specified value, or a regular expression, and returns a new string where the specified values are replaced
- search(reg): Searches a string for a specified value, or regular expression, and returns the position of the match
- toLowerCase()
- toUpperCase()

### switch code
- charCodeAt(n): Returns the Unicode of the character at the specified index
- *fromCharCode(c1,c2 ...): Converts Unicode values to characters
- codePointAt(n): switch n+1th character to UTF-16 incoded code point
- *fromCodePoint(num,...): create string from code point value.

### ETC
- concat(str): Joins two or more strings, and returns a new joined strings
- repeat(num): Returns a new string with a specified number of copies of an existing string
- trim(): Removes whitespace from both ends of a string
- length(): Returns the length of a string

