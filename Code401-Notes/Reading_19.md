# Automation

## Reading
* [Python Regular Expressions Tutorial](https://www.datacamp.com/tutorial/python-regular-expression-tutorial)
* [shutil](https://pymotw.com/3/shutil/)

## Additional Resources
### Videos
* [Automation Ideas](https://pymotw.com/3/shutil/)
* [Automating Your Browser and Desktop Apps](https://pymotw.com/3/shutil/)

### Bookmark and Review
* [Watchdog](https://pymotw.com/3/shutil/)

Regular Expressions a.k.a. "regex" are a sequence of characters that are used to check for a pattern sequence.
To use this in Python, you need to import the `re` library. An example:
```python
import re

pattern = r"Cookie"
sequence = "Cookie"

if re.match(pattern, sequence):
    print("Match!")
else: print("Not a match!")
```

| Character | What it does                                                                                            |
|:---------:|:--------------------------------------------------------------------------------------------------------|
|    `.`    | Matches any single character except the newline character.                                              |
|    `^`    | Matches the pattern at the ***start*** of the string.                                                   |
|   `\A`    | Matches ***only*** at the start of the string.                                                          |
|    `$`    | Matches at the ***end*** of the string.                                                                 |
|   `\Z`    | Matches only at the ***end*** of the string.                                                            |
|   `[]`    | Matches the set you specify within it.                                                                  |
|    `\`    | Specialized escape character and can be used in front of metacharaters to remove their speical meaning. |
|   `\w`    | Matches any single letter, digit or underscore.                                                         |
|   `\W`    | Matches any character not part of `\w`.                                                                 |
|   `\s`    | Matches a single whitespace character like: space, newline, tab, return.                                |
|   `\S`    | Matches any character not part of `\s`.                                                                 |
|   `\d`    | Matches any decimal digit 0 - 9.                                                                        |
|   `\D`    | Matches any character that is not a decimal digit.                                                      |
|   `\t`    | Matches tab.                                                                                            |
|   `\n`    | Matches newline.                                                                                        |
|   `\r`    | Matches return.                                                                                         |
|   `\b`    | Matches only at the ***beginning*** or the ***end*** of the word.                                       |
|    `+`    | Checks if the preceding character appears one or more times.                                            |
|    `*`    | Checks if the preceding character appears zero or more times.                                           |
|    `?`    | Checks if the preceding character appears ***exactly**** zero or 1 time.                                |
|   `{}`    | Checks for an explicit number of times.                                                                 |
 |   `()`    | Creates a group when performing matches.                                                                |
|   `<>`    | Creates a named group when performing matches.                                                          |

The `shutil` module includes high-level operations such as copying and archiving.

Watchdog is installed using `pip` and is a file system events and event handlers.
