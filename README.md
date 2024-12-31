# HackerRank
This repository is for Advanced Technologies and Application Development  



1.  Solve me First (Easy)


use std::io;


The program uses the std::io module to handle input/output operations. This allows us to read data from standard input


2. Main Function
The main function is the entry point of the program:


fn main() {
    let mut num_str_1 = String::new();
    let mut num_str_2 = String::new();

    Two mutable (mut) String variables (num_str_1 and num_str_2) are declared to store the input from the user. Strings are used initially because the input comes as text

    3. Reading Input
    io::stdin().read_line(&mut num_str_1).ok().expect("Failed to read line");
io::stdin().read_line(&mut num_str_2).ok().expect("Failed to read line");


The read_line method reads a line of text from the standard input and appends it to the provided String.
&mut num_str_1 and &mut num_str_2 mean the function takes mutable references to these variables to modify them directly.
.ok() checks if the operation succeeded.
.expect("Failed to read line") ensures that if an error occurs while reading input, the program will display the message "Failed to read line" and terminate.

4. Parsing the Input
let num_1: i32 = num_str_1.trim().parse().ok().expect("Please enter a valid integer");
let num_2: i32 = num_str_2.trim().parse().ok().expect("Please enter a valid integer");


The input strings (num_str_1 and num_str_2) are trimmed using .trim() to remove any leading or trailing whitespace, such as newline characters.
.parse() converts the trimmed string into an i32 (a 32-bit signed integer).
.ok() checks if the parsing was successful.
.expect("Please enter a valid integer") ensures that if parsing fails (e.g., if the input is not a number), the program will display the message "Please enter a valid integer" and terminate.


This Rust program reads two integers from the standard input, computes their sum, and prints the result. Let's break it down step by step:

1. Importing the Required Library
rust
Copy code
use std::io;
The program uses the std::io module to handle input/output operations. This allows us to read data from standard input.
2. Main Function
The main function is the entry point of the program:

rust
Copy code
fn main() {
    let mut num_str_1 = String::new();
    let mut num_str_2 = String::new();
Two mutable (mut) String variables (num_str_1 and num_str_2) are declared to store the input from the user. Strings are used initially because the input comes as text.
3. Reading Input
rust
Copy code
io::stdin().read_line(&mut num_str_1).ok().expect("Failed to read line");
io::stdin().read_line(&mut num_str_2).ok().expect("Failed to read line");
The read_line method reads a line of text from the standard input and appends it to the provided String.
&mut num_str_1 and &mut num_str_2 mean the function takes mutable references to these variables to modify them directly.
.ok() checks if the operation succeeded.
.expect("Failed to read line") ensures that if an error occurs while reading input, the program will display the message "Failed to read line" and terminate.
4. Parsing the Input
rust
Copy code
let num_1: i32 = num_str_1.trim().parse().ok().expect("Please enter a valid integer");
let num_2: i32 = num_str_2.trim().parse().ok().expect("Please enter a valid integer");
The input strings (num_str_1 and num_str_2) are trimmed using .trim() to remove any leading or trailing whitespace, such as newline characters.
.parse() converts the trimmed string into an i32 (a 32-bit signed integer).
.ok() checks if the parsing was successful.
.expect("Please enter a valid integer") ensures that if parsing fails (e.g., if the input is not a number), the program will display the message "Please enter a valid integer" and terminate.


5. Calculating and Printing the Result
   println!("{}", num_1 + num_2);


The println! macro prints the result of adding num_1 and num_2 to the standard output.
{} is a placeholder that gets replaced by the value of the expression num_1 + num_2.


This Rust program reads two integers from the standard input, computes their sum, and prints the result. Let's break it down step by step:

1. Importing the Required Library
rust
Copy code
use std::io;
The program uses the std::io module to handle input/output operations. This allows us to read data from standard input.
2. Main Function
The main function is the entry point of the program:

rust
Copy code
fn main() {
    let mut num_str_1 = String::new();
    let mut num_str_2 = String::new();
Two mutable (mut) String variables (num_str_1 and num_str_2) are declared to store the input from the user. Strings are used initially because the input comes as text.
3. Reading Input
rust
Copy code
io::stdin().read_line(&mut num_str_1).ok().expect("Failed to read line");
io::stdin().read_line(&mut num_str_2).ok().expect("Failed to read line");
The read_line method reads a line of text from the standard input and appends it to the provided String.
&mut num_str_1 and &mut num_str_2 mean the function takes mutable references to these variables to modify them directly.
.ok() checks if the operation succeeded.
.expect("Failed to read line") ensures that if an error occurs while reading input, the program will display the message "Failed to read line" and terminate.
4. Parsing the Input
rust
Copy code
let num_1: i32 = num_str_1.trim().parse().ok().expect("Please enter a valid integer");
let num_2: i32 = num_str_2.trim().parse().ok().expect("Please enter a valid integer");
The input strings (num_str_1 and num_str_2) are trimmed using .trim() to remove any leading or trailing whitespace, such as newline characters.
.parse() converts the trimmed string into an i32 (a 32-bit signed integer).
.ok() checks if the parsing was successful.
.expect("Please enter a valid integer") ensures that if parsing fails (e.g., if the input is not a number), the program will display the message "Please enter a valid integer" and terminate.
5. Calculating and Printing the Result
rust
Copy code
println!("{}", num_1 + num_2);
The println! macro prints the result of adding num_1 and num_2 to the standard output.
{} is a placeholder that gets replaced by the value of the expression num_1 + num_2.


How It Works
The program prompts the user (via standard input) to enter two numbers, one per line.
It reads and parses these inputs into integers.
The integers are added together, and the result is printed.
    
Example Run
Input:

5
7
Output:

12

###A Very Big Sum


This Rust program calculates the sum of a list of large integers, stores the result, and writes it to an output file specified by the environment variable OUTPUT_PATH. Here's a detailed breakdown of the code:


 1.  Importing Modules


use std::env;


use std::fs::File;


use std::io::{self, BufRead, Write};



* std::env: Used to interact with environment variables (OUTPUT_PATH in this case).


* std::fs::File: Allows the program to create or open a file for writing.


* std::io: Provides essential input/output functionalities, including:


* BufRead: For buffered reading of input.


* Write: For writing output to a file.



