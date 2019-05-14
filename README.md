# DC Standard Lib

This is just a toy project with no possible real world use case. If you don't really have time to spare like me, you should not take a look at this.

Unless of course, you like stuff like [Brainfuck](https://en.wikipedia.org/wiki/Brainfuck) to fidget around.

## What is DC(1)

```bash
$ man dc
```

*Did you mean: cd*

## Why a repo?

It's good to have a backup for some useful *rutines*; the idea is that they improve overtime.

## How to use?

```bash
$ dc -f stdlib.dc -
```

### Example

In this example:

1. The array `[1, 2, 3, 4, 5]` is loaded into register `a`
2. The string stored in register `A` (average) is executed
	2.1. This string is just a combination of the strings stored at `S` (sum) and `L` (len). Both operate over the register `a`
3. The top of the stack is the average of the array stored at `a`
	3.1. The result is printed by default by `A`

```bash
$ dc -f stdlib.dc -
1sa2Sa3Sa4Sa5Sa # load array into A
lAx # load Avg string and execute it
dc: stack register 'a' (0141) is empty
dc: stack register 'a' (0141) is empty
3 # top of the stack printed
```