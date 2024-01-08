# `run-jsmoo-z80-test`

This is a small Ruby script that runs the [Z80 tests](https://github.com/raddad772/jsmoo/tree/main/misc/tests/GeneratedTests/z80) included in [JSMoo](https://github.com/raddad772/jsmoo). It requires the [`json`](https://rubygems.org/gems/json) and [`z80`](https://rubygems.org/gems/z80) gems.

## Usage

```shell
run-jsmoo-z80-test <JSON-file>...
```

If `-` is passed as an argument, the script will read the JSON data from the standard input, run the tests it contains, and exit. Subsequent arguments will be ignored.

## TL;DR

Once you have installed the dependencies, clone this repository and the main branch of the JSMoo repository. Then run the script passing the test files to run as arguments:

```shell
mkdir work && cd work
git clone https://github.com/redcode/run-jsmoo-z80-test.git
git clone https://github.com/raddad772/jsmoo.git
run-jsmoo-z80-test/run-jsmoo-z80-test jsmoo/misc/tests/GeneratedTests/z80/v1/*.json
```

## Results

As of today, the JSMoo tests are not perfect and contain a few inaccuracies, so some will not pass:

```
RESULTS SUMMARY
Files: 1610 in total; 1598 passed; 12 failed
Tests: 1610000 in total; 1602680 passed; 7320 failed
```
