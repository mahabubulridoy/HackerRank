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
  
---  
**How to run**  
1. Save the code in a file, e.g., staircase.rs.
2. Compile and run the program:  
   rustc staircase.rs  
./staircase
3. Provide the input, e.g., 4, and the program will print the staircase pattern.
---  

**Example**  
**Input**  
4  
**Output**  

   __#__  
  __##__  
 __###__  
__####__   
  

##########**Mini-Max Sum**  
This Rust program calculates and prints the minimum and maximum sums of four out of five elements in an array. For example, given an array [1, 2, 3, 4, 5], the minimum sum (by excluding the largest number) is 1 + 2 + 3 + 4 = 10, and the maximum sum (by excluding the smallest number) is 2 + 3 + 4 + 5 = 14.  


**Explanation**  
1. miniMaxSum Function  
This function calculates the minimum and maximum sums of four out of five elements in the given array.  

1. **Total Sum Calculation:  
* The total sum of all elements in the array is calculated using arr.iter().sum().  
2. Finding Minimum and Maximum Values:  
* The smallest and largest values in the array are found using .min() and .max().  
3. Calculating Min and Max Sums:  
* Minimum Sum: The minimum sum is obtained by excluding the largest value: total_sum - max_value.  
* Maximum Sum: The maximum sum is obtained by excluding the smallest value: total_sum - min_value.  
4. Print the Result:  
* The results are printed in the format min_sum max_sum.
---

2. main Function  
The main function handles input and output.

1. Reading Input:  
* The program reads a single line of space-separated integers from the standard input.  
* These integers are parsed into a vector of i64 using .split_whitespace() and .map(|s| s.parse::<i64>().unwrap()).  
2. Calling the Function:  
* The parsed array is passed to the miniMaxSum function, which prints the result.
---

**Example**  
**Input**  
1 2 3 4 5  
**Execution:**  
1. Array: [1,2,3,4,5]
2. Total Sum: 1+2+3+4+5 = 15
3. Mnimum Value: 1, Maximum Value: 5
4. Minimum Sum: 15-5=10
5. Maximum Sum: 15-1 =14  
**Output**
10 14


**##########Time Conversion**  

This Rust program converts a time string in 12-hour AM/PM format into 24-hour (military) time format. For example:

* 12:00:00AM converts to 00:00:00.  
* 07:05:45PM converts to 19:05:45.
---


**Explanation**  
1. time_conversion Function  
This function converts a time string in 12-hour AM/PM format into a 24-hour format.  

1. Extract Components:  

* Extract the AM/PM period using &s[8..].  
* Extract the time (hours, minutes, seconds) using &s[0..8].  
2. Handle AM/PM Cases:  

* AM:  
    * If the hour is 12 (midnight), convert it to 0 (00:00).  
    * Otherwise, keep the hour unchanged.  
* PM:  
    * If the hour is not 12, add 12 to convert to military time.  
3. Format the Time:  

* Use the format! macro to format the converted time as a string in hh:mm:ss format.  
2. main Function  
The main function handles input and output:  

1. Read a single string input.  
2. Call the time_conversion function with the input.  
3. Print the result.
---


**How to Run**

1. Save the code in a file, e.g., time_conversion.rs.
2. Compile and run the program
   rustc time_conversion.rs  
./time_conversion
3. Provide the input, e.g., 07:05:45PM, and the program will output the converted time.
--- 

**Example**  
**Input**  
07:05:45PM  
**Execution:** 
1. Input: 07:05:45PM  
2. Period: PM  
3. Time: 07:05:45  
4. Conversion:    
    * PM and hour is 7. Add 12: 19.  
    * Result: 19:05:45.  
**Output:**
19:05:45


**#########Grading Students**  

This Rust program implements the "grading students" problem, where grades are adjusted based on specific rounding rules. The solution ensures grades follow the given criteria and handles input/output seamlessly. Below is a detailed explanation of the program and its functionality.

---  

**Problem Description**  
The program adjusts grades according to the following rules:  

1. If the grade is less than 38, it remains unchanged (failing grades are not rounded).
2. For grades 38 and above:  
* If the difference between the grade and the next multiple of 5 is less than 3, round the grade up to the next multiple of 5.
* Otherwise, leave the grade unchanged.

---

**How It Works**  
1. gradingStudents Function  
* Input: A slice of integers representing student grades.  
* Output: A vector of integers with grades adjusted based on the rules.  
**Steps:**  

1. Iterate through the grades using .iter() and apply a transformation using .map().  
2. For grades less than 38, return the grade unchanged.  
3. For grades 38 and above:  
* Calculate the next multiple of 5 using ((grade / 5) + 1) * 5.  
* If the difference between the grade and this next multiple is less than 3, round up to the multiple.  
* Otherwise, return the original grade.  
**2. main Function**  
* Handles reading input, calling the gradingStudents function, and writing the output.  
**Steps:**  

1. Read the number of grades from standard input.  
2. Parse the grades into a vector of integers.  
3. Call gradingStudents with the vector of grades to process them.  
4. Write the adjusted grades to a file specified by the OUTPUT_PATH environment variable.

---

**How to Use**  
1. Save the Code: Save the code in a file, e.g., grading_students.rs.  

2. Compile the Program:

rustc grading_students.rs  
3. Set the Output Path: Set the OUTPUT_PATH environment variable to specify the file where results will be saved:  
export OUTPUT_PATH=output.txt  
4. Run the program:  
./grading_students  
Provide input in the format:  

<number of grades>
<grade 1>
<grade 2>
...

5. View the Output: The adjusted grades will be written to the file specified by OUTPUT_PATH.

**Example**  
**Input**  
4  
73  
67  
38  
33  
**Process**  
1. Grade 73: Next multiple of 5 is 75. Difference is 75−73=2. Round up to 75.  
2. Grade 67: Next multiple of 5 is 70. Difference is 70−67=3. No Rounding  
3. Grade 38: Next multiple of 5 is 40. Difference is 40−38=2. Round up to 40.  
4. Grade 33: Failing grade. No Rounding

**Output**  
75  
67  
40  
33  

**##########Sherlock&Squares**


**Problem Description**  
Given two integers 𝑎 and 𝑏, find how many perfect square numbers lie between them, inclusive. A perfect square is a number that can be expressed as the square of an integer, such as 1,4,9,16,….  

---  

**How It Works**  
1. squares Function  
* Input: Two integers 𝑎 and 𝑏 representing the range.  
* Output: An integer representing the count of perfect squares in the range.  
**Steps:**  

1. Use the square root function to find the smallest integer 𝑠𝑡𝑎𝑟𝑡 whose square is greater than or equal to 𝑎. This is calculated as:  
𝑠𝑡𝑎𝑟𝑡=⌈√𝑎⌉  

2. Similarly, find the largest integer 𝑒𝑛𝑑 whose square is less than or equal to 𝑏:  
𝑒𝑛𝑑=⌊√𝑏⌋  
3. Calculate the count of integers between 𝑠𝑡𝑎𝑟𝑡 and 𝑒𝑛𝑑, inclusive:  
𝑐𝑜𝑢𝑛𝑡=𝑒𝑛𝑑−𝑠𝑡𝑎𝑟𝑡+1  
4. If 𝑒𝑛𝑑<𝑠𝑡𝑎𝑟𝑡, there are no perfect squares in the range, so return 0.
---
**Input/Output Explanation  
**Input Format**  
1. The first line contains an integer q, the number of queries.    
2. Each of the next q lines contains two integers, a and b, defining the range [a,b]  
**Output Format**
For each query, output the number of perfect squares in the range [a,b]  

**Example**  
**Input**  
2  
3 9  
17 24  
**Output**  
2  
0  
**Explanatoni**  
1. For the range [3,9], the perfect squares are 4 and 9, so the count is 2.  
2. For the range [17,24], there is no perfect squares, so the count is 0.

**How to run the code**  

1. Save the Code: Save the code in a file, e.g., count_squares.rs.
2. Compile the program:
   rustc count_squares.rs
3. Set the output path: set the OUTPUT_PATH environment variable to specify the file where results will be saved.
   export OUTPUT_PATH=output.txt  

4. Run the program:
   ./count_squares  
provide input in the format:
<number of queries>
<a1> <b1>  
<a2> <b2>  
... 
5. View the output: the results will be written to the file specified by OUTPUT_PATH.  
**##########LibraryFine**  

**Problem Description**  

You are required to calculate a fine based on the return date of a library book.  

The fine is calculated as follows:  

1. If the book is returned on or before the expected return date, no fine is charged.  
2. If the book is returned after the expected return date but within the same calendar month and year, the fine is 15 Hackos for each day late.    
3. If the book is returned after the expected return month but within the same calendar year, the fine is 500 Hackos for each month late.  
4. If the book is returned after the calendar year in which it was expected, the fine is fixed at 10,000 Hackos.  

---

**Explanation of the Code**    
1. Function Definition:      

* The function libraryFine takes six integer parameters:    
    * 𝑑1,𝑚1,𝑦1: The day, month, and year of the actual return date.    
    * 𝑑2,𝑚2,𝑦2: The day, month, and year of the expected return date.    
* It returns an integer representing the fine.    
2. Logic:    

* Late Year:  
    * If the book is returned after the expected calendar year (𝑦1>𝑦2), the fine is fixed at  10,000 Hackos.  
* Late Month:  
    * If the book is returned in the same calendar year (𝑦1==𝑦2) but after the expected month (
𝑚1>𝑚2), the fine is 500 Hackos per month.  
* Late Day:  
    *If the book is returned in the same calendar year and month (𝑦1==𝑦2 and 𝑚1==𝑚2) but after the expected day (𝑑1>𝑑2), the fine is 15 Hackos per day.  
* On-Time:  
    *If the book is returned on or before the expected date (𝑦1<𝑦2 or 𝑦1==𝑦2&&𝑚1<𝑚2 or 𝑦1==𝑦2&& 𝑚1==𝑚2&&𝑑1<=𝑑2), there is no fine.  
3. Input Parsing:  

* The main function reads the return date and the expected date from standard input.  
* These dates are passed to the libraryFine function.  
4. Output:  

* The calculated fine is written to a file specified by the OUTPUT_PATH environment variable.

**Input/Output**  

**Input**  
9 6 2015  
6 6 2015  

**Output**  
45  
**Explanation**  
The book was returned 3 days late in the same month and year. The fine is 15×3=45.  

---  

**How to Use** 
1. Save the code in a file, e.g., library_fine.rs
2. Compile the program:
   rustc library_fine.rs  

3. Set the OUTPUT_PATH environment variable to specify the output file:
   export OUTPUT_PATH=output.txt
4. Run the program and provide input as specified in the problem statement.


**##########HalloweenSale**  

**Problem Statement**  
You are given:  

1. p: Initial price of the first game.  
2. d: Amount by which the price decreases after each purchase.  
3. m: Minimum price that the game can drop to.  
4. s: Budget available.  
The task is to calculate the number of games you can buy without exceeding your budget.

---  
**Explanation of the Code**  
1. Function Parameters:  

p: Initial price of the first game.  
d: Decrease in price after each purchase.  
m: Minimum possible price of the game.  
s: Budget available.  
2. Logic:  

* Initialize current_price to p, total_spent to 0, and count to 0.  
* se a loop to keep buying games as long as the total spending does not exceed the budget s.  
* After each purchase:  
    *Add current_price to total_spent.  
    *Increment count.  
    *Update current_price by reducing it by d, but ensure it does not go below m.  
* Return the total number of games bought.  
3. Input Parsing:  
* The main function reads the input values and parses them into integers.  
* These values are passed to the howManyGames function.  
4. Output:  

* The result is written to a file specified by the OUTPUT_PATH environment variable.
---

**Example Input and Output**  
**Input**  
20 3 6 80  
**Output**  
6  

**Explanation**  
* Initial prices of games: [20,17,14,11,8,6]  
* Total spending: 20 + 17 + 14 + 11 + 8 + 6 = 76  
* Remaining budget: 80 -76 = 4 (not enough for the next games)  
* Total games bought: 6

**How to use**  
1. save the code in a file, e.g, how_many_games.rs.
2. compile the program:
   
rustc how_many_games.rs  

3. Set the OUTPUT_PATH environment variable to specify the output file:
   export OUTPUT_PATH=output.txt
4. Run the program and provide input as specified in the problem statement. 

**##########Sherlock&validstring**


**Explanation of the Code**  
**Functionality**  
The isValid function determines whether a string can be classified as "valid" based on the frequency of its characters. A string is considered valid if:

1. All characters have the same frequency.
2. It is possible to remove exactly one character to make all character frequencies equal.
**Steps in the Function**  
1. Build a Frequency Map:

* Count the occurrences of each character using a HashMap.  
* Example for input aabbcc:  
    * Frequency Map: {'a': 2, 'b': 2, 'c': 2}.  
2. Count Frequency of Frequencies:  

* Count how many characters share the same frequency.  
* Example for input aabbccc:  
    *Frequency Map: {'a': 2, 'b': 2, 'c': 3}.  
    *Frequency of Frequencies: {2: 2, 3: 1}.  
3. Validation Rules:  

    * If all characters have the same frequency, the string is valid.  
        * Frequency of Frequencies: {2: 3}.  
* If there are two distinct frequencies:  
    *Check if one of the frequencies is 1 and occurs exactly once.  
    *Check if the difference between the two frequencies is 1, and the higher frequency occurs only once.  
4. Return Result:  

* Return "YES" if the string meets the criteria; otherwise, return "NO".  
**Complexity**    
* Time Complexity: 𝑂(𝑛), where n is the length of the string. Building the frequency map and the frequency-of-frequencies map both take linear time.  
* Space Complexity: O(k), where k is the number of unique characters in the string.  

---  
**Example Input and Output**  
**Input**  
aabbcc  
**Output**  
YES  
**Input**  
aabbccc  
**Output** 
YES  
**Input**  
aabbcccc  
**Output**  
NO  

**How It Works**  
1. Counts the frequency of each character in the string.  
2. Analyzes the frequency counts to check if they satisfy the validity conditions.  
3. Returns "YES" if the string is valid, otherwise "NO".  


**##########Sherlock&Anagrams**  

**Explanation of the Code**  
**Problem Statement**  
The goal is to find the number of unordered pairs of substrings that are anagrams of each other. Two substrings are considered anagrams if one can be rearranged to form the other.  

**Steps in the Function**  
1. Generate Substrings:  

* Iterate over all possible substrings of the input string.  
* Sort the characters in each substring to create a "normalized" key.  
* Store the count of each normalized substring in a HashMap.  
2. Count Anagrammatic Pairs:  

* For each substring that appears n times, the number of pairs is given by the formula:  
Pairs=𝑛⋅(𝑛−1)/2  
* Sum these values for all substrings to get the total number of anagrammatic pairs.  
3. Return the Result:   

* The final result is the total count of anagrammatic pairs.    
**Complexity**  
* Time Complexity:O(n3) in the worst case, where n is the length of the string. This is due to:  
* O(n2) for generating all substrings.  
* Sorting each substring takes O(klogk), where k is the length of the substring.  
* Space Complexity: O(n2) for storing all substring keys.  

**Example Input and Output**  
**Input**  
2  
abba  
abcd  
**Output**    
4  
0  
**Explanation**  
1. For "abba":  
* Substrings: ["a", "b", "b", "a", "ab", "bb", "ba", "abb", "bba", "abba"]  
* Sorted keys: ["a", "b", "b", "a", "ab", "bb", "ab", "abb", "abb", "abba"]  
* Anagrammatic pairs: ("a", "a"), ("b", "b"), ("ab", "ba"), ("abb", "bba").  
2. For "abcd":  
* Substrings do not form any anagrams.


**##########Pairs**  
**Purpose of the Code**  
This program calculates the number of pairs of numbers in a list where the difference between the two numbers equals a given value k.  

**How it works**  
1. The pairs Function
This function does the main work:
fn pairs(k: i32, arr: &[i32]) -> i32 {  
    let mut values: HashSet<i32> = HashSet::new();  
    let mut count = 0;  

    for &num in arr {  
        if values.contains(&(num - k)) {  
            count += 1; // A pair with difference k exists  
        }  

        if values.contains(&(num + k)) {  
            count += 1; // Another pair with difference k exists  
        }  

        values.insert(num); // Add current number to the set  
    }  
  
    count // Return the total number of pairs  
}  
 * Inputs:
   * k: the target difference.
   * arr: the list of numbers to check.
* process:
  * use a HashSet to track numbers already seen.
  * for each number, check if a number exists that differs by k
  * increment the count for every valid pair found.
* Output: The total number of valid pairs.  

2. he main Function
   fn main() {  
    let stdin = io::stdin();  
    let mut stdin_iterator = stdin.lock().lines();  

    let mut fptr = File::create(env::var("OUTPUT_PATH").unwrap()).unwrap();  

    let first_multiple_input: Vec<String> = stdin_iterator.next().unwrap().unwrap()  
        .split(' ')  
        .map(|s| s.to_string())  
        .collect();  

    let n = first_multiple_input[0].trim().parse::<i32>().unwrap();  
    let k = first_multiple_input[1].trim().parse::<i32>().unwrap();  

    let arr: Vec<i32> = stdin_iterator.next().unwrap().unwrap()  
        .trim_end()  
        .split(' ')  
        .map(|s| s.to_string().parse::<i32>().unwrap())  
        .collect();  

    let result = pairs(k, &arr);  

    writeln!(&mut fptr, "{}", result).ok();  
}  


* Steps:
  1. Reads input valus for n (number of elements), k (target difference), and the list arr.  
  2. calls the pairs function with k and arr to calculate the number of pairs.  
  3. writes the result to an output file.

**Example**  
**Input**  
5 2  
1 5 3 4 2  
* k=2
* arr = [1,5,3,4,2]

**Steps**  
1. check pairs:  
   * 1: No valid pairs.  
   * 5: No valid pairs.  
   * 3:3-2 =1 (valid) and 3+2=5  
   * 4:4-2=2 valid  
   * 2: no valid pairs  
2. Total pairs =3

**Output**

3


**##########The time in words**  

This Rust program reads two integers (h and m) from standard input, representing the hour and minutes, and converts the time into a human-readable format in words (e.g., 3:00 becomes three o' clock).

---  

**Code Breakdown**  
**Imports** 
use std::env;  
use std::fs::File;  
use std::io::{self, BufRead, Write};  

* env: Used to retrieve environment variables.
* fs::File: Used to create and write to a file.
* io::{self, BufRead, Write}: Provides input/output utilities for reading from standard input and writing to files.

---  

**The timeInWords Function**  

fn timeInWords(h: i32, m: i32) -> String {
    let numbers = [
        "", "one", "two", "three", "four", "five", "six", "seven", "eight", "nine", "ten", "eleven",
        "twelve", "thirteen", "fourteen", "quarter", "sixteen", "seventeen", "eighteen",
        "nineteen", "twenty", "twenty one", "twenty two", "twenty three", "twenty four",
        "twenty five", "twenty six", "twenty seven", "twenty eight", "twenty nine", "half",
    ];  

* A numbers array maps numbers from 1 to 30 to their corresponding English words. For example, 1 maps to "one", 15 maps to "quarter", and 30 maps to "half".
* These words are used to construct the output string.

---  
**Match Expression**  
The core logic determines how the time should be represented in words based on the value of m (minutes):  

match m {  
    0 => format!("{} o' clock", numbers[h as usize]),  
    1 => format!("one minute past {}", numbers[h as usize]),  
    15 => format!("quarter past {}", numbers[h as usize]),  
    30 => format!("half past {}", numbers[h as usize]),  
    45 => format!("quarter to {}", numbers[(h % 12 + 1) as usize]),  
    2..=30 => format!(  
        "{} minutes past {}",  
        numbers[m as usize],  
        numbers[h as usize]  
    ),  
    31..=59 => format!(  
        "{} minutes to {}",  
        numbers[(60 - m) as usize],  
        numbers[(h % 12 + 1) as usize]  
    ),  
    _ => String::new(),  
}  

m == 0: Outputs the hour with "o' clock". For example, 3:00 becomes "three o' clock".  
m == 1: Outputs "one minute past {hour}".  
m == 15: Outputs "quarter past {hour}".  
m == 30: Outputs "half past {hour}".  
m == 45: Outputs "quarter to {next hour}". The next hour is calculated as (h % 12 + 1).  
2..=30: For minutes between 2 and 30, it outputs "X minutes past {hour}".  
31..=59: For minutes between 31 and 59, it outputs "X minutes to {next hour}"  

---  

**Main Function**  
The main function handles input and output:  

fn main() {  
    let stdin = io::stdin();  
    let mut stdin_iterator = stdin.lock().lines();  

    let mut fptr = File::create(env::var("OUTPUT_PATH").unwrap()).unwrap();  

    let h = stdin_iterator.next().unwrap().unwrap().trim().parse::<i32>().unwrap();  
    let m = stdin_iterator.next().unwrap().unwrap().trim().parse::<i32>().unwrap();  

    let result = timeInWords(h, m);  

    writeln!(&mut fptr, "{}", result).ok();  
}  

1. Read Input:  

* stdin.lock().lines() locks standard input and creates an iterator over its lines.  
* The first line contains the hour h, and the second line contains the minutes m. Both are parsed as i32.  
2. Environment Variable:  

* env::var("OUTPUT_PATH") retrieves the output file path from the environment.  
* File::create creates a file at that path.  
3. Compute Result:  

timeInWords(h, m) converts the given time to words.  
4. Write Output:  

writeln! writes the result to the output file.  

---  
**Example Execution**  

**Input**  
5  
45  
Execution:  
1. The hour h = 5, and minutes m = 45.  

2. In timeInWords:  
format!("quarter to {}", numbers[(h % 12 + 1) as usize])  
h % 12 + 1 == 6, so the result is "quarter to six".
3. The output "quarter to six" is written to the file specified by OUTPUT_PATH.  

---   

**Edge Cases**
1. Exact Hour:  

*Input: 6 0  
*Output: "six o' clock"  
2. One Minute Past:  

* Input: 2 1  
* Output: "one minute past two"  
3. Half Past:  

*Input: 7 30  
*Output: "half past seven"  
4. Minutes to Next Hour:  
  
*Input: 11 59  
* Output: "one minute to twelve"  
5. Invalid Input:  

* If input is empty or invalid, the program will panic because of .unwrap().  


