# Notes for Code401: Day 2

- [Java Imports](<https://perso.ensta-paris.fr/~diam/java/online/notes-java/language/10basics/import.html>)

- A group of java classes can create a package.
- A package name is the same as the folder which contains the .java files.
- Package declaration syntax
  - the statement order is:
    1. Package statement (optional but recommended)
    2. Imports (optional)
    3. Class or interface definitions

```java
package illustration;

import java.awt.*;

public class Drawing {
  ...
}
```

- Imports have 3 options:

  1. Use of the wildcard (`*`) character to specify that all classes within that package should be made available to your program
  2. Classes can be specified explicity on import
  3. Using the fully qualified class name without an import

- There are 166 packages that contain 3,279 classes and interfaces. The most common imports are:

  - java.awt.* -> (Common GUI elements)
  - java.awt.event.* -> (The most common GUI event listeners)
  - javax.swing.* -> (Move common GUI elements - Note: javax)
  - java.util.* -> (Data structures (collections), time, Scanner, etc classes)
  - java.io.* -> (I/O classes)
  - java.text.* -> (Some formatting classes)
  - java.util.regex.* -> (Regular expression classes)
