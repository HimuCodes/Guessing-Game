 **# Guess the Number Game**

**This is a simple number-guessing game written in Rust while learning from *The Rust Programming Language* book.**

**Features:**

* Generates a random number between 1 and 100.
* Prompts the user to guess the number.
* Provides feedback on whether the guess is too high, too low, or correct.
* Uses colored text for a more engaging experience (requires the `colored` library).

**How to Play:**

1. Run the program using `cargo run` (or `rustc main.rs && ./main`).
2. The game will prompt you to input your guess.
3. Enter a number between 1 and 100 and press Enter.
4. The game will provide feedback on your guess.
5. Keep guessing until you get the correct number!

**Code Structure:**

1. **Use Statements:**
   - `use rand::Rng;`: Imports functionality for generating random numbers.
   - `use std::cmp::Ordering;`: Provides comparison methods for numbers.
   - `use std::io;`: Allows for input/output operations.
   - `use colored::*;`: Enables colored text output (from the `colored` crate).

2. **Main Function:**
   - Generates a random number using `rand::thread_rng().gen_range(1..=100)`.
   - Starts a loop that continues until the correct number is guessed.
     - Prompts the user for input.
     - Reads the user's guess from the console.
     - Parses the guess into a u32 number.
     - Compares the guess to the secret number using `cmp`.
     - Provides feedback based on the comparison.
     - Prints a victory message and breaks the loop if the guess is correct.

**Dependencies:**

* The `colored` crate is required for colored text output. Install it using `cargo add colored`.

**Learning Objectives:**

- This project demonstrates basic Rust concepts such as:
    - Variables and data types (u32, String)
    - User input/output (print, read_line)
    - Control flow (loop)
    - Comparison operators (match)
    - String manipulation (trim, parse)
    - Error handling (expect)
    - Random number generation (rand::Rng, gen_range)
    - Using external crates (colored)
