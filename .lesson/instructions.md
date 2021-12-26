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
