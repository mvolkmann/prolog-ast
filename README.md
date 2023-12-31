# prolog-ast

This demonstrates using Prolog to implement a custom programming language.

The demo language is called Less Is More (LIM).
For an example of the syntax, see `demo.lim`.

The commands described next assume you have installed Scryer Prolog
and have defined the alias `scry` to run the `scryer-prolog` command.

To compile the file `demo.lim` to an abstract syntax tree (AST),
run the script `limc` with `./limc demo.lim`.
This creates the file `demo.limb` that contains an AST
represented by a single Prolog term which is a nested structure.

To execute the AST, run the script `lim` with `./lim demo.limb`.

The AST uses the following mapping from supported actions to Prolog functor names:

| Action              | Functor Name |
| ------------------- | ------------ |
| assignment          | `a`          |
| function call       | `c`          |
| function definition | `f`          |
| constant            | `k`          |
| math expression     | `m`          |
| print               | `p`          |
| program             | `pr`         |
| return              | `r`          |
