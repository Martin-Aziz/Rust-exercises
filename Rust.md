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
