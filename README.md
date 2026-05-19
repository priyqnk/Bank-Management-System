# Bank Management System

A C++ project that models a bank account database using multiple **hash table** collision-resolution strategies. Each strategy is implemented as a polymorphic subclass sharing a common interface for account and transaction operations.

## Features

The following hashing schemes are implemented behind a shared `BaseClass` interface:

| Strategy | Collision handling |
|----------|-------------------|
| **Chaining** | Separate chaining with linked structures |
| **Linear probing** | Sequential search for the next open slot |
| **Quadratic probing** | Probe sequence based on a quadratic function |
| **Cubic probing** | Probe sequence based on a cubic function |
| **Comp** | Comparative / composite hashing strategy |

### Core operations

- `createAccount` — Insert a new account
- `addTransaction` — Record a transaction for an account
- `getTopK` — Retrieve top-K accounts by a ranking criterion

## Tech Stack

| Component | Technology |
|-----------|------------|
| Language | C++11 |
| Design | Abstract base class with virtual methods |

## Project Structure

```
Bank-Management-System/
├── BaseClass.h              # Abstract interface
├── Chaining.cpp / .h
├── LinearProbing.cpp / .h
├── QuadraticProbing.cpp / .h
├── CubicProbing.cpp / .h
├── Comp.cpp / .h
├── test.cpp                 # Driver and test cases
├── run.sh                   # Build and run script
└── README.md
```

## Getting Started

### Prerequisites

- g++ with C++11 support

### Installation

```bash
git clone https://github.com/priyqnk/Bank-Management-System.git
cd Bank-Management-System
```

### Build and run

Using the provided script:

```bash
bash run.sh
```

Or compile manually:

```bash
g++ -std=c++11 -o bank_test test.cpp Chaining.cpp Comp.cpp CubicProbing.cpp LinearProbing.cpp QuadraticProbing.cpp
./bank_test
```
