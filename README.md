toy-brainfuck
-------------

A little toy Brainfuck interpreter.

This is an interpreter for the
[Brainfuck language](https://en.wikipedia.org/wiki/Brainfuck), written
in Haskell. I just wanted to see what writing something like this would
be like.

Brainfuck is a dual-tape Turing Machine:
- The command tape is read-only, and its symbols are characters
- The data tape is read/write, and its symbols are integers

The following command symbols are recognized:
- **`>`**: Shift the data head to the right
- **`<`**: Shift the data head to the left
- **`+`**: Increment the symbol under the data head
- **`-`**: Decrement the symbol under the data head
- **`.`**: Print the symbol under the data head to stdout
- **`,`**: Read a symbol from stdin, and write it to the data head
- **`[`**: Jump forward to the matching `]` if the data head reads zero
- **`]`**: Jump back to the matching `[` if the data head does not read zero
- All other characters are no-ops

(All symbols also shift the command head to the right)
