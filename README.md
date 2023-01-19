# nekontrol - Control your kattis solutions

This is a simple program that compiles, runs and tests your kattis solutions
against local and sample input and output.

## Demo

### Successful run

![Demo of a succesful run](./res/demo1.svg)

### Incorrect output

![Demo of an unsuccessful run](./res/demo2.svg)

## Features

- Automatically downloads sample input and output
- Discovers local sample input and output
- Compiles your source code and runs it with local and sample input and output
- Ignores debug messages - ignores lines starting with "dbg" or "debug" and
  inline messages "(dbg...)" and "(debug...)". If debug lines are discovered
  then you are notified in the output so that you don't submit something that is
  incorrect.

The current supported languages are:

- C++
- Rust
- Python
  > **Note**
  > Runs with `pypy3` for kattis compatibility
- Haskell

Adding more languages are left as an exercise for the reader.

## Usage

Simply run `nk <source file>` and it should hopefully compile (if needed)
and run!

- `nk` assumes that the name of the source files matches the name of the
  problem (found in the url, ex. https://open.kattis.com/problems/<b>hello</b>).
  If this assumption is incorrect, you can specify the problem with
  `--problem <problem name>`. Local files are still matched with the filename
  regardless of the problem specified.
- Input and output files should follow the format `<filename>.in` or
  `<filename>.<number>.in` and corresponding outputs are named `<filename>.ans`
  etc. where `<filename>` comes from `nk <filename>.cpp` for instance.

> **Note**
> Multiple support files are not supported as of yet

## Installation

```sh
git clone https://github.com/Quaqqer/nekontrol.git
cd nekontrol
pip install .
```

Now it should hopefully work, enjoy!

### Nix

There is also a flake for Nix users, but if you use Nix I trust you know how to
use flakes.

## Other

- If you are thinking "nekontrol is a kinda weeby name", I ask you: have you
- ever tried coming up with an original name?
