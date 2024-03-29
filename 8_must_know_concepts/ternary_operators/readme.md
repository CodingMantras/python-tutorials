# Ternary conditional operators

Using a conditional operation in a single line as a switch to get one or another value. Ternary specifically means having three inputs.

## Syntax

```bash
[value_if_true] if [condition] else [value_if_value]
```

## Example

```python
a = 4
b = 9

max_value = a if a > b else b
# It means, max_value will be a if a is greater than b, otherwise b

print(max_value)
# Output: 9
```

## How is it different from an if condition?

If we need to do a different thing depending on the condition we use if-condition. But sometimes we use ternary conditional operator to compute the value and then do something with the result.

## Using multiple conditions in a ternary operators

[false_value, true_value](test)

Example:

```python
time_in_hrs = int(time.strftime("%H"))

greeting = "Good Morning" if 0 < time_in_hrs < 12 else "Good After Noon" if 12 <= time_in_hrs < 18 else "Good Evening"
print(greeting)
# Output: As per the computer time"
```

## Using ternary operators in a tuple

### Syntax for ternary in a tuple

```(false_value, true_value)[test]```

or

```x, y = (1, 2) if condition else (3, 4)```

### Example for ternary in a tuple

```python
a = 4
b = 9
value = (a, b)[a > b]
print(value)
# As the test fails here, so the false will evaluate
# Output: 4
```
