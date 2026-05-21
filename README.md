<p align="center">
  <img src="logos/logo_bg.png" width="150" height="150" alt="HolyPy Logo">
</p>

# HolyPy Support

Visual Studio Code extension providing language support for **HolyPy**, a custom programming language designed for the Compilers course (ECOM06) at UNIFEI.

## Features

- **Syntax Highlighting**: Comprehensive colorization for HolyPy keywords, types, operators, and literals.
- **Language Configuration**: Smart brackets, auto-closing pairs, and comment toggling.
- **File Support**: Automatically recognizes `.hpy` files.

## Language Overview

HolyPy is a statically typed language with a focus on simplicity and low-level control.

### Keywords
- **Control Flow**: `if`, `else`, `cycle`, `free`, `return`
- **I/O & Declaration**: `let`, `fn`, `speak`, `receive`, `import`
- **Memory & Low-level**: `chain`, `unchain`, `asm`

### Types
- **Integers**: `i8`, `i16`, `i32`, `i64` (signed) and `u8`, `u16`, `u32`, `u64` (unsigned)
- **Floats**: `f32`, `f64`
- **Others**: `char`, `bool`, `u0` (void)

### Operators
- **Arithmetic**: `+`, `-`, `*`, `/`, `mod`
- **Comparison**: `==`, `!=`, `>`, `<`, `>=`, `<=`
- **Logical**: `and`, `or`, `not`

## Example Code

```holypy
# This is a comment
fn main() -> u0 {
    let message = "Hello, HolyPy!";
    speak(message);
    
    if (true) {
        cycle {
            # Loop logic
            break;
        }
    }
}
```

## Requirements

No additional dependencies are required. Just install the extension and start coding in HolyPy!

## Installation

1. Open **Visual Studio Code**
2. Go to **Extensions** (Ctrl+Shift+X)
3. Search for **holypy-support**
4. Click **Install**

## Known Issues

None at the moment. If you find any bugs, please report them on the project repository.

## Release Notes

### 0.0.1
- Initial release of HolyPy support.
- Basic syntax highlighting and language configuration.

---

**Developed as part of the ECOM06 - Compilers course at UNIFEI.**


