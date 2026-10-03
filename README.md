# Haskell JSON Parser

A small JSON parser written in Haskell, based on the [Coding Challenges](https://codingchallenges.fyi/) challenge series by John Crickett. The project explores building a parser from combinators rather than relying on a JSON parsing library.

## What it does

- Defines a minimal parser type that consumes a `String` and returns either a parsed value with the remaining input or failure.
- Builds JSON-oriented parsers for objects, arrays, strings, numbers, and the `true`, `false`, and `null` literals.
- Represents parsed JSON values with a small set of Haskell data types in `Main.hs`.

This is an in-progress learning project, not a complete or standards-compliant JSON implementation. In particular, string escapes and full JSON number validation are not implemented yet. The current program reads `test.json` and prints parser output; the sample files under `jsons/` are not currently run as an automated test suite.

## Files

- `Parser.hs` — parser combinators and the `Parser` type.
- `Main.hs` — JSON value types, JSON parsers, and the executable entry point.
- `test.json` — input read by the current executable.
- `jsons/` — sample JSON inputs retained in the repository.

## Run

Requires [GHC](https://www.haskell.org/ghc/).

```sh
ghc Main.hs -o hjp
./hjp
```

The executable expects to be run from the repository root because it reads `test.json` using a relative path.
