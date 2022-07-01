# Code Pattern

This documentation will show some important rules to standardize our code and thus keep it readable and easy to maintain.

----
## Javascript
<br>

### #1 - Name Pattern

Always use the CamelCase pattern for naming your variables and functions and use the PascalCase pattern for component names.

Examples:

```
const currentItem // CamelCase

const CurrentItem // PascalCase
```

**Note:** Always use English to name your functions, components, and variables

<br>

### #2 - Use names that reveal your purpose

The names of variables and functions must be clear.

Examples:

```
const n = 'John Doe' // Bad name

const clientName = 'John Doe' // Good name
```

Note that by using clear names, you also make these names easier to find when performing a search, in the above case you may notice that the name **n** is not searchable because many results will be found for this search, since the name **clientName** is more specific and therefore easier to find.

**Note:** Always use **const** and **let** to declare variables.

<br>

### #3 - Magic numbers

Magic numbers are those random numbers that from time to time you end up finding in the code, they are "magical" because they resemble a magician's trick, requiring an explanation for them to be understood.

Example:

```
if (password.length() > 7) {
  throw new PasswordException("InvalidPasswordSize");
}
```

Note that in the example above it was necessary to read the exception message so that we could understand why that number **7** was there. To keep our code more readable we avoid the use of these magic numbers, and to solve the above example just create a variable with a relevant name and use it.

Example:

```
const maxPasswordSize = 7
if (password.length() > maxPasswordSize) {
  throw new PasswordException("InvalidPasswordSize");
}
```

<br>

### #4 - DRY (Don't repeat yourself)

DRY says that each piece of knowledge in a system must have a unique representation and be completely unambiguous. In other words, it defines that there cannot be two parts of the program that perform the same function.

DRY should be applied to both functions and structure, if you notice a value will be repeated several times in your code, consider putting it in a global or local variable.

<br>

### #5 - Stuck texts

Never leave text stuck in your code, whenever you need to use text, be it to represent a message to the user or a label for a field on your form.

Use the i18n-js library to manage any text you need to put in your code, including in the case of internationalization of your applications.

[Doc's i18n-js](https://www.npmjs.com/package/i18n-js)

<br>

## CSS

For CSS use the **Stitches** library, in case of creating new classes that do not have in the library, use the **DRY** writing pattern, for other cases use the **Stitches** library.

[Doc's stitches for react](https://stitches.dev)

[Doc's stitches for angular](https://stitches.dev/docs/framework-agnostic)

[Doc's DRY](https://meiert.com/en/blog/dry-css/)
