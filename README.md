# Rust Hello World Example

A minimal Rust implementation of "Hello, World!" that demonstrates basic Rust syntax and compilation using just the Rust compiler (`rustc`). This example deliberately avoids build systems like Cargo to show the fundamentals of Rust compilation.

## Prerequisites

You'll need the Rust compiler (`rustc`) installed on your system. You can install it using platform-specific package managers:

### Linux
Using apt (Debian/Ubuntu):
```bash
sudo apt update
sudo apt install rustc
```

Using dnf (Fedora):
```bash
sudo dnf install rust
```

### macOS
Using Homebrew:
```bash
brew install rust
```

### Windows
Download the Rust installer from https://www.rust-lang.org/tools/install and run it. This will install `rustc` and add it to your PATH.

## Compiling

The compilation process is the same across all platforms, though the output filename differs on Windows:

### Linux and macOS
```bash
rustc main.rs -o hello
```

### Windows
```cmd
rustc main.rs -o hello.exe
```

## Running

### Linux and macOS
```bash
./hello
```

### Windows
```cmd
hello.exe
```
Or from PowerShell:
```powershell
.\hello.exe
```

## Code Explanation

Let's examine our implementation line by line:

```rust
fn main() {
    println!("Hello, World!");
}
```

The code demonstrates several fundamental Rust concepts:

1. The `fn main()` declaration defines the program's entry point. Every Rust executable needs this function.

2. The `println!` macro (note the `!` which indicates it's a macro, not a function) handles formatted printing to stdout. Rust uses macros for operations that need to be evaluated at compile time or require variable numbers of arguments.

## Verifying the Build

You can verify that your program was built without any unnecessary dependencies by examining the binary size and its dependencies:

### Linux
```bash
# Check binary size
ls -l hello
# Check dynamic dependencies
ldd hello
```

### macOS
```bash
# Check binary size
ls -l hello
# Check dynamic dependencies
otool -L hello
```

### Windows
```cmd
dir hello.exe
dumpbin /dependents hello.exe
```

## Further Reading

- [The Rust Reference](https://doc.rust-lang.org/reference/introduction.html)
- [rustc Command Manual](https://doc.rust-lang.org/rustc/index.html)
