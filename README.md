# Calling Rust from Python with PyO3

Author: Cong Vo (congvm.it@gmail.com)

## Introduction

This is a simple example of how to call Rust code from Python using PyO3.
With this approach, you can write performance-critical code in Rust and use it in Python, especially in data science and machine learning projects.

## Requirements

- Python 3.6 or later
- Rust 1.45 or later
- PyO3
- Maturin
- Cargo


## Installation and Usage

```bash
pip install maturin

cd hello-rust

# Build the Rust code and install the Python package
maturin develop

python -c "import hello_rust; print(hello_rust.add(1, 2))"
# Or 
cd py && python test.py


# Build production wheels
maturin build --release
```

## Project Structure

```
.
├── Cargo.lock
├── Cargo.toml
├── README.md
├── py
│   └── test.py
├── pyproject.toml
└── src
    └── lib.rs

3 directories, 6 files
```

## Refencences

[1] https://hackernoon.com/calling-rust-from-python-with-pyo3 \
[2] https://pyo3.rs