# Lesson 3: numbers

## Booleans

The only values for the boolean data type are `True` and `False`. The special function `bool()` can convert any Python data type to a boolean, by following the convention that nonzero numbers are considered `True` and nonzero are considered `False`.

```Python
bool(True)
bool(1)
bool(10)
bool(-20)
bool(0)
bool(0.0)
bool(False)
```

We will see how this is useful later on.

## Integers
### Definition
Integers are, as in Math, whole numbers. As expected, a sequence of digits specifies a positive integer:

```Python
0
5
42
-10
```

Commas cannot be placed as thousands separators, but underscores can serve that purpose (they are simply ignored so their purpose is merely cosmetic):

```Python
1000000
1_000_000
1000000 == 1_000_000
1_0_0 == 100
```

### Integer arithmetic

Integer operators work as expected, with the integer division `//`and the modulus operator `%` as the ones that depart from what we typically see in a calculator:

| Operator | Description | Example | Results |
|----------|-------------|---------|---------|
| +        | Addition    | 2 + 2   | 4       |
| -        | Subtraction | 10 - 5  | 5       |
| \*       | Multiplication | 4 * 2 | 8      |
| /        | Floating-point division | 10 / 4 | 2.5 |
| //       | Integer division | 7//2 | 3     |
| %        | Modulus (remainder) | 7%3 | 1   |
| \*\*     | Exponentiation | 2 ** 5 | 32    |

Also, note that the `^` that other languages such as R use for exponentiation is not valid in Python.

Let's try a few examples:

```Python
4 + 4
20 - 8
4 + 2 + 3 - 5
5 * 8
2 * 2 * 3
9 / 5
9 // 5
```
Note that the blanks surrouding the operators are not necessary, but enhance readibility.

Remember that, since a variable is a name that points to an object, operations like `a - 2` do not change `a`, so if we really want to change the variable we need to do:
```Python
a = a - 2
```
which is equivalent to:
```Python
a = 10
temporary = a - 2
a = temporary
```

These type of arithmetic operators with assignments can be compressed with the following shortcuts: `+=`, `-=`, `*=`, `/=`, etc. Let's try a few examples:

```python
b = 10
b = b + 1
b
b += 1
c = 10
c = c - 1
c -= -1
d = 2
d = d * 2
d *= 2
e = 20
e = e / 10
e /= 10
f = 20
f = f // 13
f //= 13
g = 10
g %= 7
h = 2
h = h ** 2
h **= 3
j = 0
j **= 0
```

The commands `//` and `%` can be combined with the `divmod()` function:

```python
divmod(10, 3)
```
which provides the result in a two-item named _tuple_, which we will revisit soon.

### Precedence

Precedence rules can catch one by surprise, so one should either memorize precedence rules or add parenthesis in case of doubt (the latter is safer):

```python
-3 ** 2
(-3) ** 2
```

