# YACC

[![Build Status](https://travis-ci.com/spenserblack/yacc.svg?branch=master)](https://travis-ci.com/spenserblack/yacc)

Yet Another Coloring Crate

# What's the Difference?

This crate provides a macro for coloring strings, allowing ANSI colors to be set at compile time instead of runtime.

# Example

```rust
println!(yacc!("It {;green}!"), "works");
println!(yacc!("Warning: {:#?;yellow}!"), Err(()));
```

## Features

This crate *should* support all format options defined in
[`std::fmt`](https://doc.rust-lang.org/std/fmt/). If it's missing something (and it probably will
before v1.0.0), submit an Issue or PR!

After defining formatting (like `:?` or `:#?`), you define coloring with `;color`. So, to print
debug format in red, `{:?;red}`.
