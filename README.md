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

**###A Very Big Sum**


This Rust program calculates the sum of a list of large integers, stores the result, and writes it to an output file specified by the environment variable OUTPUT_PATH. Here's a detailed breakdown of the code:


 **1.  Importing Modules**


use std::env;


use std::fs::File;


use std::io::{self, BufRead, Write};



* std::env: Used to interact with environment variables (OUTPUT_PATH in this case).


* std::fs::File: Allows the program to create or open a file for writing.


* std::io: Provides essential input/output functionalities, including:


* BufRead: For buffered reading of input.


* Write: For writing output to a file.


**2. Function Definition**

fn aVeryBigSum(ar: &[i64]) -> i64 {


    // Sum up all elements in the array `ar` and return the result


    ar.iter().sum()

    
}


* Purpose: Takes a slice of 64-bit integers (&[i64]) as input and returns their sum as a 64-bit integer (i64).

  
*Key Operations:


    *ar.iter(): Creates an iterator over the elements of the slice.
    *.sum(): Iterates through all elements, summing them up. The type inference ensures that the summation works with i64.


3. **Main Function**



fn main() {

The entry point of the program where the input is read, processed, and the output is written.

**Reading Input**

    let stdin = io::stdin();

    
    let mut stdin_iterator = stdin.lock().lines();

*io::stdin(): Accesses the standard input stream.


*stdin.lock().lines(): Creates an iterator to read lines from the input. Using a locked buffer ensures efficient reading.

**Preparing the Output File**

    let mut fptr = File::create(env::var("OUTPUT_PATH").unwrap()).unwrap();


*env::var("OUTPUT_PATH"): Retrieves the value of the environment variable OUTPUT_PATH, which specifies the output file's path.


*File::create: Creates or opens the file for writing. If the file cannot be opened, unwrap() will panic.

**Processing Input**

    let _ar_count = stdin_iterator.next().unwrap().unwrap().trim().parse::<i32>().unwrap();


*Reads the first line of input and parses it as an integer (i32), representing the count of numbers. Although it's read, this value is not used in the program.

    let ar: Vec<i64> = stdin_iterator.next().unwrap().unwrap()
        .trim_end()
        .split(' ')
        .map(|s| s.parse::<i64>().unwrap())
        .collect();
Reads the second line of input, which contains space-separated integers.


*trim_end(): Removes any trailing whitespace (e.g., newlines).  
*split(' '): Splits the string by spaces to isolate each integer as a substring.  
*map(|s| s.parse::<i64>().unwrap()): Parses each substring into a 64-bit integer (i64).  
*.collect(): Converts the iterator into a vector of integers (Vec<i64>).  








