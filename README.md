# HackerRank
This repository is for Advanced Technologies and Application Development  



##########1.  Solve me First (Easy)


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

**##########A Very Big Sum**


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


* trim_end(): Removes any trailing whitespace (e.g., newlines).  
* split(' '): Splits the string by spaces to isolate each integer as a substring.  
* map(|s| s.parse::<i64>().unwrap()): Parses each substring into a 64-bit integer (i64).  
* .collect(): Converts the iterator into a vector of integers (Vec<i64>).

  
**Calling the Function**


  let result = aVeryBigSum(&ar);
  * The aVeryBigSum function is called with a reference to the vector ar, and the computed sum is stored in result.


**Writing Output**

    writeln!(&mut fptr, "{}", result).ok();


* writeln!: Writes the result (sum of the array) to the file specified by fptr, followed by a newline.  
* ok(): Silently handles any potential write errors by ignoring them.

**Overall Flow**


1. Input Handling:  
* Read the size of the array (not directly used).
* Parse the integers into a vector of i64.
2. Computation:  
* Calculate the sum using the aVeryBigSum function.
3. Output Handling:  
* Write the result to the specified output file.

**Key Advantages**  
* Safety: unwrap() ensures errors are caught immediately (though it will panic if an error occurs).  
* Efficiency: Uses buffered input and direct file output for high performance.  
* Clarity: The logic is cleanly separated into input processing, computation, and output


##########**Diagonal Difference**

use std::io;  
* The std::io module is used for input and output operations. In this program, we use it to read user input from the standard input.

**1. diagonalDifference Function**  
fn diagonalDifference(arr: Vec<Vec<i32>>) -> i32 {  
    let n = arr.len();  
    let mut primary_diagonal_sum = 0;  
    let mut secondary_diagonal_sum = 0;  
* **Purpose:** This function computes the absolute difference between the sums of the two diagonals in a square matrix.  
**Parameters:**  
* arr: A 2D vector (Vec<Vec<i32>>) representing the square matrix.  
**Variables:**  
* n: The size of the square matrix (number of rows or columns).
* primary_diagonal_sum: Stores the sum of the primary diagonal (top-left to bottom-right).
* secondary_diagonal_sum: Stores the sum of the secondary diagonal (top-right to bottom-left).

**Iterating Through the Matrix**  
    for i in 0..n {  
        primary_diagonal_sum += arr[i][i]; // Sum of primary diagonal  
        secondary_diagonal_sum += arr[i][n - i - 1]; // Sum of secondary diagonal  
    }  
* This loop iterates over each row (i) in the matrix:  
    * Primary diagonal: Accessed using arr[i][i] (same row and column index).  
    * Secondary diagonal: Accessed using arr[i][n - i - 1] (row i and column n - i - 1).


**For example:**  
* For row 0, primary diagonal is arr[0][0], secondary diagonal is arr[0][n-1].  
* For row 1, primary diagonal is arr[1][1], secondary diagonal is arr[1][n-2]

**Calculating the Absolute Difference**  
    (primary_diagonal_sum - secondary_diagonal_sum).abs()  
}  
* Compute the difference between the two diagonal sums.  
* Use .abs() to return the absolute value.  
This function returns the result as an i32 integer.

**2. main Function**  
The main function handles input and output.  

**Reading the Size of the Matrix**  
    let mut input = String::new();  
    io::stdin().read_line(&mut input).unwrap();  
    let n: usize = input.trim().parse().unwrap(); // Read the size of the matrix  
* A new string, input, is created to store the input data.  
* io::stdin().read_line(&mut input).unwrap() reads a single line of input and stores it in input.  
* The line is trimmed of extra whitespace using .trim() and parsed into a usize (unsigned integer) to represent the size of the matrix (n).

**Reading the Matrix Rows**  
    let mut arr: Vec<Vec<i32>> = Vec::new();  

    for _ in 0..n {  
        input.clear();  
        io::stdin().read_line(&mut input).unwrap();  
        let row: Vec<i32> = input  
            .trim()  
            .split_whitespace()  
            .map(|x| x.parse::<i32>().unwrap())  
            .collect();  
        arr.push(row);  
    }  
1. **Matrix Initialization:** An empty 2D vector arr is created to store the matrix.  
2. ##Loop Through Rows:##
* For each row of the matrix (from 0 to n-1):  
    * Clear the input string to read the next line of input.    
    * Read the row as a single line.  
    * Split the line by spaces using .split_whitespace().  
    * Convert each space-separated value into an i32 using .map(|x| x.parse::<i32>().unwrap()).  
    * Collect the parsed integers into a vector and add it to the 2D vector arr using .push(row).
 
  **Calling the Function and Printing the Result**

      let result = diagonalDifference(arr);  
    println!("{}", result);
* The diagonalDifference function is called with the matrix arr, and the result is stored in result.  
* The result is printed to the console.


**Example Execution**  
**Input**  
3  
11 2 4  
4 5 6  
10 8 -12   
**Step-by-Step Execution:**  
1. Read Matrix Size:  
* n = 3  
2. **Read Matrix:**  
* First row: [11, 2, 4]  
* Second row: [4, 5, 6]  
* Third row: [10, 8, -12]  
* Final matrix
[  
    [11, 2, 4],  
    [4, 5, 6],  
    [10, 8, -12]  
]  
3. **Diagonal Sums**  
  * Primary diagonal: 11 + 5 + (−12) = 4  
  * Secondary diagonal: 4 + 5 + 10 = 19  
4. ** Abdolute Difference:  
    * ∣4−19∣=15  
**Output** 
15  


#############**Staircase**


This Rust program prints a right-aligned staircase pattern of size n using the # symbol. For example, if n = 4, the staircase would look like this:  


   __#__  
  __##__  
 __###__  
__####__    

**Explanation**  
1. **Purpose:**  

        * The staircase function prints a staircase pattern of size n, where each row has increasing numbers of # symbols, right-aligned by spaces.  
2. **Input:**  

        * The program reads an integer n from the standard input, which determines the height and width of the staircase.  
3. **How It Works:**  

        * The for loop iterates from 1 to n (inclusive), representing each row of the staircase.  
* **Spaces:**  
        * For each row i, the number of spaces is calculated as n - i, and they are generated using " ".repeat((n - i) as usize).  
* **Hashes:**  
        * The number of # symbols is equal to the row number i, generated using "#".repeat(i as usize).
The line is constructed by concatenating the spaces and hashes and printed to the console using println!.
4. **Output:**
      * For n = 4, the output would be:
  
   __#__  
  __##__  
 __###__  
__####__  

5. **Main Function:**  

        * Reads the integer input n from the standard input using the BufRead trait.  
        * Calls the staircase function with n to print the staircase.
**How to run**  
1. Save the code in a file, e.g., staircase.rs.
2. Compile and run the program:
   rustc staircase.rs  
./staircase
3. Provide the input, e.g., 4, and the program will print the staircase pattern.

**Example**  
**Input**  
4  
**Output**  

   __#__  
  __##__  
 __###__  
__####__   
  











