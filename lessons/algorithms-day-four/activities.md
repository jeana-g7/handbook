---
title: Activity
order: 2
---

## Wordy

- Given a sentence, find the length of the shortest word

## Change, please

Given any amount of change from zero cents to 99 cents, determine the minimum
number of coins to make change. Consider only quarters, dimes, nickels, and
pennies.

For example: 6 cents = 1 penny, 1 nickle, 0 dimes, 0 quarters 11 cents = 1
penny, 0 nickles, 1 dime, 0 quarters 43 cents = 3 pennies, 1 nickle, 1 dime, 1
quarter

## Colorful Triangles

From: https://www.codewars.com/kata/5a25ac6ac5e284cfbe000111/train/ruby

A colored triangle is created from a row of colors, red, green or blue. Each
containing one fewer color than the last, successive rows are generated by
considering the two touching colors in the previous row. If these colors are
identical, the same color is used in the new row. If they are different, the
missing color is used in the new row. This is continued until the final row,
with only a single color, is generated.

The different possibilities are:

```
Colour here:        G G        B G        R G        B R
Becomes color:      G          R          B          G
```

With a more significant example:

```
R R G B R G B B
 R B R G B R B
  G G B R G G
   G R G B G
    B B R R
     B G R
      R B
       G
```

You will be given the first row of the triangle as a string, and it is your job
to return the final color, which would appear in the bottom row as a string. In
the case of the example above, you would the given `RRGBRGBB` you should return
`G`.

## Calculator

When writing math formulas, we work in what is known as "infix" notation. For
instance `5 + ((1 + 2) * 4) - 3`. We can use the
[PEDMAS](https://en.wikipedia.org/wiki/Order_of_operations#Mnemonics) rule.
(Parentheses, Exponents, Multiplication/Division, Addition/Subtraction)

However, there is another way to represent these operations. This is known as
"Reverse Polish Notation." The description "Polish" refers to the nationality of
logician Jan Łukasiewicz who invented Polish notation in 1924.

If you ever used an older style Hewlett Packard Calculator, you've experienced
RPN.

The statement `5 + ((1 + 2) * 4) - 3` in RPN would be: `5 1 2 + 4 * + 3 -`

To evaluate this, you would take the sequence `1 2 +` and turn that into a `3`,
then apply the `4 *` (12), then we would apply `5 +`, and finally `- 3`

Your job is to create a calculator which evaluates expressions in Reverse Polish
notation. The value of the RPN above is `14`