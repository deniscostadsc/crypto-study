# Modulo operation

This notebook is aimed to place all the study about modulus function

## Definition

Modulos operation finds the remainder after a division of one number by another[\[1\]](https://en.wikipedia.org/wiki/Modulo_operation)[\[2\]](https://youtu.be/W1SY6qKZrUk?t=1m19s)

Let's say $a$, $r$, $m \in \mathbb{Z}$ and $m > 0$:

$a \equiv r \mod m \text{, if } m \vert (a - r)$

### Definition verification

$a = 13 \text{, } m = 9 \text{ and }r = ?$

$13 \equiv 4 \mod 9$

Then we go back to the "if" part of the definition:

$ m \vert (a - r)$

$9 \vert (13 - 4)$

$9 \vert 9$

The we we got $9 \vert 9$, that is true, because 9 is divisible. 

## Computation of the remainder

Here, $q$ is the quotient.

$a = q \cdot{m} + r$

Example:

$a = 42$ and $m = 9$

$42 = 4 \cdot{9} + 6$

To verify this we can use the definition above:

$9 \vert (42 - 6)$

$9 \vert 36$ that is true.

## Congruence (or Equivalent) classes

Let's to see on practice. The example above (when $a = 42$ and $m = 9$) can be rewritten as $42 = 3 \cdot{9} + 15$, which is also true, as you can see below:

$42 = 3 \cdot{9} + 15$

Let's verify this:

$9 \vert (42 - 15)$

$9 \vert 27$ that is also true.

Or also

$42 = 5 \cdot{9} + (- 3)$

Let's also verify this:

$9 \vert (42 - (- 3))$

$9 \vert (42 + 3)$

$9 \vert 45$, that, of course, it is true.

**That means that based on that definition above, there are many possible remainders, in other words, the remainder is not unique**

When $a = 42$ and $m = 9$, and looking the examples right above, we came with the following congruence class:

$\{..., -14, -3, 6, 15, 24, ...\}$

To generate a congruence class for $\mod 9$, for example, we start with 0 (that is a possible $r$ to $\mod 9$):

$\{..., 0, ...\}$

To add the positive items add 9 (remember we are generating the congruence classes for $\mod 9$) to zero:

$\{..., 0, 9, ...\}$

And keep doign this:

$\{..., 0, 9, 18, 27, ...\}$

To get the negative number, you should subtract 9:

$\{-9, 0, 9, 18, 27, ...\}$

And keep doing this:

$\{..., -18, -9, 0, 9, 18, ...\}$

This set is infinite. To get the next class you do the same logic but you start with $1$:

$\{..., -19, -8, 1, 10, 19, ...\}$

And you do this until $9 - 1$. In this case until 8. All possible congruence class for $\mod 9$ are:

$\{..., -18, -9, 0, 9, 18, ...\}$

$\{..., -19, -8, 1, 10, 19, ...\}$

$\{..., -18, -7, 2, 11, 20, ...\}$

$\{..., -17, -6, 3, 12, 21, ...\}$

$\{..., -16, -5, 4, 13, 22, ...\}$

$\{..., -15, -4, 5, 14, 23, ...\}$

$\{..., -14, -3, 6, 15, 24, ...\}$

$\{..., -13, -2, 7, 16, 25, ...\}$

$\{..., -12, -1, 8, 17, 26, ...\}$

All congruence classes conbined covers the whole set of $\mathbb{Z}$. **If we pick any item in the congruence class as an $r$, it will behave the same**

To explain this let's name all the $\mod 9$ congrunce classe:


$\{..., -18, -9, 0, 9, 18, ...\}$ is $A$

$\{..., -19, -8, 1, 10, 19, ...\}$ is $B$

$\{..., -18, -7, 2, 11, 20, ...\}$ is $C$

$\{..., -17, -6, 3, 12, 21, ...\}$ is $D$

$\{..., -16, -5, 4, 13, 22, ...\}$ is $E$

$\{..., -15, -4, 5, 14, 23, ...\}$ is $F$

$\{..., -14, -3, 6, 15, 24, ...\}$ is $G$

$\{..., -13, -2, 7, 16, 25, ...\}$ is $H$

$\{..., -12, -1, 8, 17, 26, ...\}$ is $I$

Let' try one example we already used to validate all items in a congruence class behave the same:

$42 = $

## References

[1] - https://en.wikipedia.org/wiki/Modulo_operation

[2] - https://youtu.be/W1SY6qKZrUk?t=1m19s

[3] - https://en.wikipedia.org/wiki/Modular_arithmetic
