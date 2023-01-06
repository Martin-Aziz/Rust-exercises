## Basics 
###### Program Ouputs Comments and its Different Styles
```rust
fn main() {
    // This is our first program in this course 
    // This is the second line of comment

    /* this is 
    a 
    multiple line 
    comment 
    */
   
   
    // This is a printing function
    println!("Hello from rust program");

   // comments inside a command
    print/*ln*/!("Hello, world!");
	
    // learning some basic output commands
    println!("The value of the constant is {}",10);

    // Learning to print strings 
    println!("My first name is {} and my last name is {}","Nouman", "Azam");

    // Learning the print command 
    print!("This is a print command "); 
    print!("This is going to be printed on the same line");

    // Learing to write on multiple lines
    print!("\nThis is going to be
            Printed on multiple 
            line"); 
        
    // Learning the use of escape sequences 
    println!("\\n\n This is going to be printed after two lines. \t This will have a tab");

    // Learning somes uses of back slash.
    println!("This will print single quote \' and this double quotes \"");
    println!("This is going to print one back slash \\") ;
    print!("This is some text which will be overwritten \r this text will only appear on the screen");

    // Learning Positional Arguments
    println!("\nI doing {2} from {1} years and i {0} it","like",20,"programming"); 

    // learning Named Arguments 
    println!("{language} is a system progrmaming language which is cool to {activity} in.", language="Rust", activity = "code");
    
    // learning to print basci maths 
    println!("The summation of 25 + 10 = {}", 25 +10);

}
```
#### Variables in Rust 
```rust
fn main() {
    let mut x = 15;  
    println!("the value of variable x = {}",x); 
    
    x  = 60; 
    println!("the value of variable x = {}",x); 

    let y = 5 *5; 
    

    // --------------------------------------
    // 			Data Types 	
    // --------------------------------------


    // --------------------------------------
    // 			Scalar Data Types
    //	 		- Integers 
    //				- Singed i8, i16, i32, i64, i128	
    //				- Unsigned u8, u16,u32,u64, u128	
    // --------------------------------------


    println!("The Maximum number in i8 = {}", std::i8::MAX);
    println!("The Maximum number in u8 = {}", std::u8::MAX);

    // --------------------------------------
    // 			- Floats 	
    //				- f32, f64
    // --------------------------------------

    let z = 3.65;
    println!("The addition of an integer and float is {}",x+z);
    println!("The Maximum number in f32 = {}", std::f32::MAX);

    // --------------------------------------
    // 			- Boolean  	
    // --------------------------------------

    let status = false; 
    println!("The value of some of our variables are {:?}", (x,y,z,status));

    let not_equals = 18 != 18;   // you can use > < >= or <=
    println!("The value of condition is 18! = 18 is {}", not_equals);

    // --------------------------------------
    // 			- Characters 	
    // 				- Represent single letters, 
    //  			- digit, 
    //				- emoji's or 
    //				- unicode scalar values	
    // --------------------------------------

   

    let c1 = 'a';
    let c2 = '3';
    let c3 = '+';
    let c4 = '\u{288A}'; 
    let c5 = '\"'; 
    println!("The value of c1 is {}, c2 is {}, c3 is {}, c4 is {} and c5 is {}",c1,c2,c3,c4,c5);


}


```
### Initializing mutliple variables 
```rust
fn main() {


   let (first_number, second_number) = (250, 480.32); 
   println!("The first number is {} and the second number is {}", first_number, second_number);

    // -------------------------------------------------
    // 			Readability of large numbers
    // -------------------------------------------------

    let large_number = 1_000_000; 
    println!("The value of the large number is {}", large_number);


    // -------------------------------------------------
    // 			Integer Overflow 
    // -------------------------------------------------
    
    //let overflow_number:u8 = 256; 
    
   
    // -------------------------------------------------
    // 			Decimal numbers in other formats
    // -------------------------------------------------
    

    let x= 255; 
    println!("The value of the variable x in hexademical is {:o} and in octal is {:X} and in binary {:b}",x,x,x);
    

    // -------------------------------------------------
    // 			Snake case convention for variables
    // -------------------------------------------------

    // Snake case convention for variable names 
    let Number = 45; // define as let number:i32 = 45  
	
    // -------------------------------------------------
    // 			Operations on number in 
    // 			different formats
    // -------------------------------------------------

	let n1 = 14; 
	let n2 = 15.6; 			
	let n3 = n2 as i32+ n1;         
	println!("The value of n3 = {}",n3);

    // -------------------------------------------------
    // 			Shadowing 
    // -------------------------------------------------
 	
    // Case 1: simple shadowing
    println!("\n***************************************************** \n");

    //let s = 5; 
    //let s = 5*5; 
    //println!("The value of the variable s = {}",s); 

    // Case2: shadowing with mut. it will work 
    //    let mut s = 5; 
    //  let s = 5*5; 
    //println!("The value of the variable s = {}",s); 

   // Case 3: we can change the type ith shadowing also
    /*let s = 32; 
    println!("The variable s = {} is currently an integer",s);
    let s = 'A'; 
    println!("The variable s = {} is currently a character",s);
    let s = 64.5;     
    println!("The variable s = {} is currently a float",s);
    */

    // Case 4: The shadowing in case of code segments
    let mut s = 65; 

    {
        s = 60; // after this change s to let s = 60 and will change the output to 65
	println!("The value of the variable s inside the inner scope = {}",s); 
    }
    println!("The value of the variable s = {}",s); 

    // -------------------------------------------------
    // 			Constants 
    // -------------------------------------------------

    const MAX_SALARY: u32 = 100_000;
    println!("The value of the constant is {}", MAX_SALARY);

}
```
### Strings		 - Fixed length strings (&str)
```rust
fn main() {
let some_string = "Fixed length string"; 
println!("The text inside the string is \"{}\" ",some_string); 


    // -------------------------------------------------
    // 			Strings
    // 			 - Variable length strings 
    // -------------------------------------------------

let mut growable_string = String::from("This string will grow");  
println!("The text inside the string is \"{}\" ",growable_string); 

    // -------------------------------------------------
    // 			Strings
    // 			 - Adding removing characters/strings 
    // -------------------------------------------------

growable_string.push('s');
println!("hey The text inside the string is \"{}\" ",growable_string); 

// Removing one last character 
growable_string.pop(); 
println!("The text inside the string is \"{}\" ",growable_string); 

// Adding some string to the string 
growable_string.push_str(" which i will use");
println!("The text inside the string is \"{}\" ",growable_string); 

    // -------------------------------------------------
    // 			Strings
    // 			 - Functions on strings 
    // -------------------------------------------------

println!("I am going to tell you some basic thing about the string,
Is the string emtpy {}, 
The length of the string is {},
The string has {} bytes, 
Does the string contains the word 'use' {},",growable_string.is_empty(),
growable_string.len(),  
growable_string.capacity(),
growable_string.contains("use"));

growable_string.push_str("   "); 
println!("Length of the string before trim is {},
Length of the string after the trim is {}",growable_string.len(), growable_string.trim().len()); 


// Number to string 
let number = 6;
println!("The value of number in string is {}", number.to_string()); 
println!("Is the number really a string {}", number.to_string() == "6"); 

// chars to string
let some_char = 'a'; 
print!("The value of character in string is {}, 
Is the character really a string {}",some_char.to_string(),some_char().to_string == "a");  

let my_name = "nouman azam".to_string(); 
println!("This string contains my name {}", my_name);


    // -------------------------------------------------
    // 			Strings
    // 			 - Creating an empty string
    // -------------------------------------------------

let empty_string = String::new();
println!("length is {}",empty_string.len()); 

    // -------------------------------------------------
    // 			Strings
    // 			 - Formatting and concatenating strings 
    // -------------------------------------------------

let s_1 = "Nouman".to_string();
let s_2 = "Azam".to_string();
let s_3 = format!("My first name is {}, and my last name is {}",s_1,s_2);
println!("{}",s_3);

// Concatenating strings 
let string_1 = String::from("Nouman");
let string_2 = String::from("Azam"); 
let string_3 = format!("{}{}", string_1,string_2);
println!("The concatenated string is {}",string_3);


}

```
 ### Tuples
 ```rust
 fn main() {



let my_information= ("Salary", 40_000);
println!("{} is equal to {}",my_information.0,my_information.1); 
println!("Another way of printing the whole tuple is {:?}", my_information);


let (salary, salary_value ) = my_information;
println!("The values of the individual variables are, 
{} and {}",salary, salary_value ); 

let salary = my_information.0;
let salary_value = my_information.1; 
println!("The values of the individual variables are, 
{} and {}",salary, salary_value );

let nested_tuple = (4, 5.0, (3, 2), "Hello");  
let element = nested_tuple.2.0;   // or (nested_tuple.2).0, in some earlier version the syntax will be (nested_tuple.2).0
println!("The value of element is {}", element); 

  
empty_tuple  = (); 


    // -------------------------------------------------
    // 			Arrays
    //			- Declaring arrays
    //	 		- Accessing elements
    //	 		- Printing elements
    //	 		- Updating elements 
    //	 		- Initializing with same values
    //	 		- String and char arrays
    //	 		- Array slices
    //	 		- Accessing elements
    //	 		- Common functions 
    //	 		- Invalid access 
    // -------------------------------------------------

let mut number_array: [i32; 5] = [4,5,6,8,9];  

// Printing a specific element
println!("{}",number_array[0]);

// Printing the whole array 
println!("{:?}",number_array);

// Updating a specific number 
number_array[4] = 5; 
println!("{:?}",number_array);

// Initiallizing arrays with same elements 
let array_with_same_elements = [0;10];

// String arrays 
let mut string_array_1 = ["apple","tomato","grapes"];
let string_array_2 = ["Unknown";6]; 
string_array_1[0] = "kamran azam"; 

// Character Arrays 
let char_array = ['a','p','p','l','e']; 

// array slices
let mut number_array_1: [i32; 5] = [4,5,6,8,9];
let subset_array = &number_array_1[0..3];    // [0..=3]  
println!("The subset of values of the array are {:?}",subset_array); 

// Number of elements in an array 
println!("Elements in the array are {}", number_array_1.len());

// Number of bytes the array is occupying 
/* if we change the type of numbers from i32 to 
i64 then it will occupy more bytes */ 
println!("The array is occupying {} bytes", std::mem::size_of_val(&number_array_1)); 

// Invalid access 
// number_array_1[10] = 5; 

// Check if the elements exists
let check_index = number_array_1.get(100); 
println!("{:?}", check_index);


}

 ```
 ## Vectors
 ```rust
 fn main(){
// declaring vectors 
let mut number_vec:Vec<i32> = vec![4,5,6,8,9,10,11,12,15,16,12,10];  

// Printing a specific element
println!("{}",number_vec[0]);

// Printing the whole vector 
println!("{:?}",number_vec);

// Updating a specific element 
number_vec[4] = 5; 
println!("{:?}",number_vec);

// Initiallizing vectors with same elements 
let array_with_same_elements: Vec<i32> = vec![0;10];

// String vectors 
let mut string_array_1: Vec<&str> = vec!["apple","tomato","grapes"];
let string_array_2: Vec<&str> = vec!["Unknown";6]; 
string_array_1[0] = "kamran azam"; 

// Character vectors 
let char_array: Vec<char> = vec!['a','p','p','l','e']; 

// Get subset of an vector without making a copy but by reference
let subset_vec = &number_vec[0..3];  // the concept of borrow 
println!("The subset of values of the array are {:?}",subset_vec); 

// Number of elements in an array 
println!("Elements in the array are {}", number_vec.len());

// Check if the elements are there or not 
let check_index = number_vec.get(100); 
println!("{:?}", check_index);

// Adding elements to the vector using the push 
number_vec.push(30);
number_vec.push(40);
println!("The subset of values of the array are {:?}",number_vec); 

// Removing element from the vector 
number_vec.remove(5); 
println!("The array after removing the element at index 5 {:?}",number_vec);

// Checking for an item inside a vector
println!("The value of 10 exist in the array {}",number_vec.contains(&10)); 
}
 ```
 
