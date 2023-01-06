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

