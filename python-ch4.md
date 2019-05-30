# Python Primitive Types

## Operators

### AND

```python
x & y
# Bitwise "and"
# If x and y are both 1, then evaluates to 1
# If x and y evals to x being 1 and y 0, then 0
```

### OR

```python
x | y
# Bitwise "or"
# If x or y is 1, then evals to 1
# If x and y is 0, then evals to 0  
```

### COMPLEMENT

```python
# The complement of something basically is reverse
~x # If x is 0, then ~x is 1
```

### EXCLUSIVE OR

```python
x^y
'''Each bit of the output is the same as the corresponding
bit in x if that bit in y is 0.
It's the complement of the bit in x if that bit in y is 1.
'''
# Examples
# If x is 1 and y is 0, then evals to 1, because y is 0, x is 1
# If x is 0 and y is 1, then evals to 1, because y is 1, ~x is 1
# If x is 1 and y is 1, then evals to 0, because y is 1, ~x is 0
# If x is 0 and y is 0, then evals to 0, because y is 0, x is 0
```

### BITWISE SHIFT TO LEFT

```python
x << y
'''Returns x with the bits shifted to the left by y places
(and new bits on the right-hand-side are zeros).
This is the same as multiplying x by 2**y. '''

'''You can use the bin function of Python to convert a bitwise
operation to binary numbers to see the bits shifted to left or
right, for more clarity'''

bin(1 << 0)
# '0b1' - shift by 0 bits to left, 1 is the current binary number
bin(1 << 1)
# '0b10' - shift by 1 bit to the left, 10 is binary number, aka
# int('10', 2) where first arg is binary number and second arg
# is base, base 2 for binary, equals decimal number 2.
bin(1 << 2)
# '0b100' - shift by 2 bits left, 100 is binary number
# aka 4
bin(1 << 10)
# 1 * 2**10 = bin(1024) aka '0b10000000000'
```

### BITWISE SHIFT TO RIGHT

```python
x >> y
'''
Similar to bitwise shift to left, but now to right.
Same as x//2**y (fractions) - // means int division'''

bin(1 >> 1)
# '0b0', aka 1//2**1 = 1/2

bin(2 >> 1)
# '0b1', aka 2//2**1 = 1

bin(4 >> 1)
# '0b10', aka 4//2**1 = 2
```
## Other Notes

- Negative numbers are represented in binary with a leading `1`.
- Positive numbers start with `0` in binary

## Steps to Convert Decimal to Binary

If you don't have a calculator to hand, you can easily convert a decimal number to binary using the remainder method. This involves dividing the number by 2 recursively until you're left with 0, while taking note of each remainder.

- Write down the decimal number.
- Divide the number by 2.
- Write the result underneath.
- Write the remainder on the right hand side. This will be 0 or 1.
- Divide the result of the division by 2 and again write down the remainder.
- Continue dividing and writing down remainders until the result of the division is 0.
- The most significant bit (MSB) is at the bottom of the column of remainders and the least significant bit (LSB) is at the top.
- Read the series of 1s and 0s on the right from the bottom up. This is the binary equivalent of the decimal number.

### Example

```
Convert decimal 100 to binary.

100/2 = 50
Remainder = 0 (LSB)
50/2 = 25
Remainder = 0
25/2 = 12 remainder 1
12/2 = 6, r0
6/2 = 3, r0
3/2 = 1, r1
1/2 = 0, r1 (MSB)
=======
1100100

Check bin('1100100') = 100
```

Source: Owlcation
<https://owlcation.com/stem/How-to-Convert-Decimal-to-Binary-and-Binary-to-Decimal>
