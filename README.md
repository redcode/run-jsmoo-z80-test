# `run-jsmoo-z80-test`

This is a small Ruby script that runs the [Z80 tests](https://github.com/raddad772/jsmoo/tree/main/misc/tests/GeneratedTests/z80) included in [JSMoo](https://github.com/raddad772/jsmoo). It has been written at the request of the [author](https://github.com/raddad772) of JSMoo to check the validity of the tests and help in their improvement. It requires the [`json`](https://rubygems.org/gems/json) and [`z80`](https://rubygems.org/gems/z80) gems.

## Usage

```shell
run-jsmoo-z80-test <JSON-file>...
```

If `-` is passed as an argument, the script will read the JSON data from the standard input, run the tests it contains, and exit. Subsequent arguments will be ignored.

Examples:

```shell
# Run the script with specific JSON files
run-jsmoo-z80-test file1.json file2.json

# Run the script with JSON data from standard input
echo '<JSON>' | run-jsmoo-z80-test -
```

## TL;DR

Once you have installed the dependencies, clone this repository and the main branch of the JSMoo repository. Next, run the script, passing it the paths to the JSON files you want to process:

```shell
mkdir work && cd work
git clone https://github.com/redcode/run-jsmoo-z80-test.git
git clone https://github.com/raddad772/jsmoo.git
run-jsmoo-z80-test/run-jsmoo-z80-test jsmoo/misc/tests/GeneratedTests/z80/v1/*.json
```

## Results

The [`z80`](https://rubygems.org/gems/z80) gem passes the full set of [Z80 tests](https://github.com/raddad772/jsmoo/tree/main/misc/tests/GeneratedTests/z80) included in [JSMoo](https://github.com/raddad772/jsmoo):

```
RESULTS SUMMARY
Files: 1610 in total; 1610 passed
Tests: 1610000 in total; 1610000 passed
```
