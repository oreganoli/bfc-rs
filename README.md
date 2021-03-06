# BFC-RS

BFC-RS is a feature-complete [Brainfuck](https://en.wikipedia.org/wiki/Brainfuck) compiler for x86_64 Linux implemented in Rust.

## Features

- generates a working executable for any Brainfuck program
- optimizes programs at compile time to reduce disk space/memory usage and execution time
- optionally produces an assembly code dump for manual inspection

## Manual building and installation
`cargo build` and `cargo install` are entirely adequate.

## Dependencies

BFC-RS requires `nasm` and `ld` to be available.
## Usage
```
bfc-rs <source_filename> [-o <output-filename>] [--dump-nasm] [--no-cleanup]
Options:
  -o, --output-filename
                    output filename (must be provided unless --dump-nasm is
                    explicitly passed)
  --no-cto          disable compile-time optimizations
  --dump-nasm       instead of compiling, print raw NASM output to stdout for
                    debugging
  --no-cleanup      do not clean up build directory after successful build
  --help            display usage information
```

## Licensing and attribution

As this code has to do with Brainfuck, we're already using the word "fuck", so I'd ordinarily see nothing wrong with licensing this code under the WTFPL. However, this repository uses the [`argh` library](https://github.com/google/argh/), whose MIT license isn't compatible with that, as well as [Daiki Maekawa](https://github.com/DaikiMaekawa/)'s [brainfuck-echo](https://github.com/DaikiMaekawa/brainfuck-echo/) program used in the course of developing BFC-RS.

BFC-RS itself also uses the MIT license.
