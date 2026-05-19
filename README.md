# Bank Management System (Hashing Implementation)

A C++ project exploring various hashing strategies and collision resolution techniques in the context of a bank account database.

## Features

This system implements several hashing classes derived from a common `BaseClass`:

- **Chaining**: Handles collisions using linked lists (or vectors).
- **Linear Probing**: Resolves collisions by searching for the next available slot sequentially.
- **Quadratic Probing**: Uses a quadratic function to find the next available slot.
- **Cubic Probing**: Uses a cubic function for probing.
- **Comp**: A comparative hashing strategy.

## Technical Highlights

- **Polymorphism**: Uses an abstract base class with virtual functions for database operations like `createAccount`, `addTransaction`, and `getTopK`.
- **Hasing Algorithms**: Implements custom hash functions for string IDs.

## Usage

### Compilation
You can use the provided `run.sh` script or compile manually:
```bash
g++ -o bank_test test.cpp Chaining.cpp Comp.cpp CubicProbing.cpp LinearProbing.cpp QuadraticProbing.cpp
```

### Running Tests
```bash
./bank_test
```
