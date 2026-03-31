# Simple Grep in C

## Description

A lightweight command-line utility written in C that searches for a substring (pattern) in a file or from standard input.

This project is a minimal implementation of basic `grep` functionality using standard C library functions such as `fgets` and `strstr`.

---

## Features

* Search for a pattern in a file
* Read input from standard input (stdin)
* Line-by-line processing
* Uses only standard C library
* Simple and minimal design

---

## Usage

```bash
./program pattern [file]
```

### Arguments

* `pattern` — the substring to search for
* `file` (optional) — file to read from

If no file is provided, the program reads from standard input.

---

## Examples

### Search in a file

```bash
./program hello file.txt
```

### Using stdin

```bash
cat file.txt | ./program hello
```

### Manual input

```bash
./program hello
```

Then type text manually and press `Ctrl+D` to finish input.

---

## How It Works

The program follows this algorithm:

1. Reads command-line arguments
2. Determines input source (file or stdin)
3. Reads input line by line using `fgets`
4. Searches for the pattern using `strstr`
5. Prints matching lines to stdout

---

## Build

Compile using GCC:

```bash
gcc -o program main.c
```

---

## Limitations

* Fixed maximum line length (`MAX_LINE`)
* Case-sensitive search
* No support for regular expressions
* Does not handle very large files optimally

---

## Possible Improvements

* Add case-insensitive search (`-i`)
* Print line numbers (`-n`)
* Support multiple files
* Implement manual substring search (without `strstr`)
* Add regex support
* Handle long lines dynamically (using `getline`)

---

## Project Structure

```bash
.
├── main.c
└── README.md
```

---

## Learning Goals

This project helps to understand:

* File I/O in C (`fopen`, `fgets`, `fclose`)
* String processing (`strstr`)
* Command-line arguments (`argc`, `argv`)
* Standard streams (`stdin`, `stdout`, `stderr`)

---

## License

This project is open-source and available under the MIT License.
