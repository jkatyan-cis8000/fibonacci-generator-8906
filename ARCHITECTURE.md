# ARCHITECTURE.md

Written by team-lead before spawning teammates. This is the shared blueprint —
teammates read it to understand what they are building and how their module fits.
Update it when the structure changes; do not let it drift from the actual code.

## Module Structure

- `fibonacci.py`: Core Fibonacci generation logic with iterative algorithm
- `cli.py`: Command-line interface for user interaction
- `tests/test_fibonacci.py`: Unit tests for the Fibonacci generator

## Interfaces

- `fibonacci.py` exposes:
  - `generate_fibonacci(limit: int) -> list[int]`: Returns list of Fibonacci numbers up to limit
  - `get_fibonacci_number(n: int) -> int`: Returns the nth Fibonacci number
- `cli.py` depends on fibonacci module for generation logic
- `tests/test_fibonacci.py` depends on fibonacci module for testing

## Shared Data Structures

- Input: `limit` (int) - upper bound for Fibonacci numbers
- Output: `list[int]` - sequence of Fibonacci numbers where each number <= limit

## External Dependencies

- None required - pure Python standard library implementation
