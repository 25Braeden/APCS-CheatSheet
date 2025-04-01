# Everything you should know for APCS

Fairly in-depth breakdown of everything that we've covered in class this year, along with possibly some helpful tricks I picked up.

## Table of Contents

> [!NOTE]
> I'm organizing this by unit according to college board. If rushed on time check [here](https://apcentral.collegeboard.org/courses/ap-computer-science-a) to see which topics you should prioritize.

- [Unit 1: Primative Types](#java-primitive-types)
- Unit 2: Using Objects
- Unit 3: Boolean Expressions and If Statements
- Unit 4: Iteration
- Unit 5: Writing Classes
- Unit 6: Array
- Unit 7: ArrayList
- Unit 8: 2D Array
- Unit 9: Inheritance
- Unit 10: Recursion

## Java Primitive Types

In Java, **primitive types are the most basic kinds of data** — things like numbers, characters, and booleans. They are **not objects**, which means they don’t have methods (you can't do `int.someMethod()`), and they’re stored more efficiently in memory.

> 🧠 **Why it matters**: Since primitives aren’t objects, they behave differently than things like `String` or `ArrayList`. You can’t call methods on them or use `.equals()` — you use `==` to compare them directly.

### 🎯 Focus for the AP Exam

The **AP Computer Science A exam** mainly focuses on these four primitives:

| **Type**  | **Example**            | **Description**                      |
| --------- | ---------------------- | ------------------------------------ |
| `int`     | `int x = 42;`          | Whole numbers                        |
| `double`  | `double pi = 3.14;`    | Decimal numbers (floating-point)     |
| `boolean` | `boolean flag = true;` | True or false logic                  |
| `char`    | `char c = 'A';`        | Single characters (in single quotes) |

Other types (`byte`, `short`, `long`, `float`) **exist**, but you **likely don’t need to know them** for the exam.

---

### ✅ Quick Reference Table

| **Type**  | **Size** | **Example**            | **Notes**                             |
| --------- | -------- | ---------------------- | ------------------------------------- |
| `int`     | 32 bits  | `int x = 5;`           | Used for most whole numbers           |
| `double`  | 64 bits  | `double d = 3.14;`     | Default for decimals                  |
| `boolean` | ~1 bit   | `boolean isOn = true;` | Only values: `true` or `false`        |
| `char`    | 16 bits  | `char letter = 'A';`   | Represents a single Unicode character |

> 💡 **Tip**: Characters use single quotes (`'A'`), while strings use double quotes (`"Hello"`). Mixing them up causes compiler errors!

---

### 🛠️ Not Objects? What Does That Mean?

- You can't use `.equals()` or call methods on primitive values.
- You compare primitives with `==` (e.g., `if (x == 5)`).
- Wrapper classes (`Integer`, `Double`, `Boolean`, `Character`) exist if you _need_ object-like behavior (like putting primitives in an `ArrayList`).

```java
int x = 5;
Integer objX = x;  // Auto-boxing: converting primitive to object
ArrayList<char> someList; // -> DOESNT WORK
ArrayList<Character> someList; // -> Does work, as we wrapped the primitive type in an object

char someChar = 'a';
char otherChar = 'a';
if (someChar == otherChar) // -> this WOULD run as you can use == to evaluate primitives
```
