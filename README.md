# Everything you should know for APCS

Fairly in-depth breakdown of everything that we've covered in class this year, along with possibly some helpful tricks I picked up.

## Table of Contents

> [!NOTE] <br />
> I'm organizing this by unit according to college board. If rushed on time check [here](https://apcentral.collegeboard.org/courses/ap-computer-science-a) to see which topics you should prioritize.

- Unit 1: Primative Types
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

In Java, there are **8 primitive types**, and most of them are **signed**, meaning they can represent both positive and negative values.

### ✅ List of Primitive Types with Ranges

| **Type**  | **Bits** | **Min Value**                | **Max Value**               | **Notes**                      |
| --------- | -------- | ---------------------------- | --------------------------- | ------------------------------ |
| `byte`    | 8        | `-128`                       | `127`                       | 2⁷ range (signed)              |
| `short`   | 16       | `-32,768`                    | `32,767`                    | 2¹⁵ range                      |
| `int`     | 32       | `-2,147,483,648`             | `2,147,483,647`             | 2³¹ range                      |
| `long`    | 64       | `-9,223,372,036,854,775,808` | `9,223,372,036,854,775,807` | 2⁶³ range                      |
| `float`   | 32       | ~`-3.4028235e+38`            | ~`3.4028235e+38`            | Approximate (IEEE 754)         |
| `double`  | 64       | ~`-1.7976931348623157e+308`  | ~`1.7976931348623157e+308`  | Approximate (IEEE 754)         |
| `char`    | 16       | `'\u0000'` (0)               | `'\uffff'` (65,535)         | **Unsigned** Unicode character |
| `boolean` | 1 (JVM)  | `false`                      | `true`                      | No numeric range               |

---

### 🔍 Notes

- All numeric types are **signed**, except for `char`, which is **unsigned**.
- Use wrapper class constants to access limits in Java code:

```java
System.out.println(Byte.MAX_VALUE);     // 127
System.out.println(Integer.MIN_VALUE);  // -2147483648
System.out.println(Character.MAX_VALUE); // 65535

```
