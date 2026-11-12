### If
```rust
fn main()
{
 
   // -------------------------------------------
   // 			Condition If 
   // 			- Simple If 
   // 			- If with multiple conditions
   // 			- If else 
   // 			- If else if ladder 
   // -------------------------------------------

   // 1. Simple if statement 
   /* General Syntax 

   if condition {
       // statements to execute if condition proves true
   }
   */ 

   // Example 
   /*
    let some_number = 40; 
    if some_number < 50 {
        println!("The number is less than 40"); 
    } 
    println!("This line will execute irrespective of the condition above"); 
  */ 
    
   /* 
   let marks  = 65; 
   if marks >= 60 && marks <= 70 {
       println!("The grade is satisfactory"); 
   }
   */ 

   
   /*
   let flag_1 = true; 
   let flag_2 = false; 
    
   if flag_1 == true || flag_2 == true {     
   
       println!("One of the condition is true here"); 
   }
   

    let flag_1 = true;  
    if flag_1 != false {     
       println!("This will execute when flag_2 is true or in other words 
       when flag_2 is not false"); 
    }
   */ 

   /*
   let flag_1 = true; 
   let flag_2 = false; 
   let number = 60; 

   // flag_1 = true && (flag_2 = false || number <50) and 
   // (flag_1 = true && flag_2 = false) || number <50

   if flag_1 == true && flag_2 == false || number < 50 {
       println!("This part will execute based on the condition above"); 
   }
   */

   // 3. If else conditions 
   /* General syntax 

   if condition {
       // Statements to execute if the condition is ture 
   }
   else {
       // Statements to execite in case the condition is false
   } 
   */ 

   /*
   let marks = 80; 
   if marks > 50 {
       println!("You have passed the exam"); 
   } else {
       println!("You have failed the exam"); 
   } 
   */

   
   /* General syntax 

   if condition {
       // Statements to execute if condition is true 
   }
   else if condition_2 {
       // Statements to execute if condition is true 
   }
   else if condition_3 { 
       // Statements to execute if condition is true 
   }
   else   // optional
   {
       // Statements to execute if all conditions are not true
   }
   */

   
   let marks = 95; 
   let mut grade = 'N'; 
   if marks >= 90 {  
       grade = 'A'; 
   } else if marks >= 80  {
       grade = 'B';
   } else if marks >=70 { 
       grade = 'C';
   } else if marks >=60  {
       grade = 'D';
   } else {             // Deleting the else block will still compile however we may have not condition being true
       grade = 'F'; 
   }

   println!("The obtained grade is {}",grade);
   
}
```
#### Nested If
```rust
fn main()
{
  // -------------------------------------------
  // 			Condition If 
  // 			- Nested If
  // 			- If let 
  // 			- If let (in case of if else ladder)   
  // 			- Match expression 	
  // -------------------------------------------

   /*     
   if outer_condition {
       // Statement to execute if the outer_condition is true 
       if inner_condition {
           // Statements to execute if both the outer and inner conditions are true 
       } else { 
           // some statements to execute
        }

    else {
        // some statements to execute
    }
    }
   */  


   // Example 
   /*
   println!("Enter a Number"); 
   let mut some_num = String::new();
   std::io::stdin()
       .read_line(&mut some_num)
       .expect("failed to read input.");
   let some_num: i32 = some_num.trim().parse().expect("invalid input");
   
   // Outer condition 
   if some_num != 0 {     // !(some_num == 0) this is equal to sum_num != 0
       // inner if condition
       if some_num % 2 == 0 {
           println!("The number is even.");
       } else {  // inner else condition 
           println!("The number is odd.");
       }  
   } else {      // outer else condition
       println!("The number is 0 and it is neither even nor odd.");
   }
   */


   // 2. if let 
   /*
   let variable_name = if condition {
       // Statements to execute and 
       // return value of variable without a semicolon 
   } else {
       // Statements to execute and 
       // value of variable of variable without a semicolon 
   };  // semicolon 
   */ 

    /*   
   let value = if true {
       1
   } else {
       2   // 2.0 will generate an error 
           // please note that the returns from all the statements should be of the same type 
           // The else part must exist otherwise the variable may be empty which the rust wont allow
   }; 
   println!("Value = {}", value); 
   */ 

   let marks = 50; 
   
   let grade = if marks >= 90 {  
       'A' 
   } else if marks >= 80  {
       'B'
   } else if marks >=70 { 
       'C'
   } else if marks >=60  {
       'D'
   } else {             // Deleting the else block will not compile 
       'F' 
   };

   println!("The obtained grade is {:?}",grade);


}
```
#### Match Statement
```rust
fn main()
{ 
  // -------------------------------------------
  // 			Match
  // 			- Simple match
  //			- If else ladder into a match
  // 			- If let syntax style match
  // -------------------------------------------
/* General syntax 

   match value {

       possible_value(s) => {Statements to execute},
       possible_value(s) => {Statements to execute},
       possible_value(s) => {Statements to execute},
          
       _ = { default_execution_statements },
   };
*/    
    /*
   let some_number = 100; 
   match some_number {
       1 | 2 => println!("The number is -1"),  
       2 | 3 => println!("The number either 2 or 3"), //    please note a single pipe here for the conditional OR
       4..=100 => println!("The number is between 4 and 100 inclusive"),       
       //_ => println!("The number is greater than 100"), 
   }
   */

    
   /*
   let marks = 50; 
   let mut grade = 'N'; 

   match marks {
   90..=100 => grade = 'A', 
   80..=89  => grade = 'B', 
   70..=79  => grade = 'C',
   60..=69  => grade = 'D',
   _ =>       grade = 'F',
   }
   println!("The grade achieved is {}",grade);
   */
   

/*    
      let variable = match value {
       possible_value(s) = {Statements to execute},
       possible_value(s) = {Statements to execute},
       possible_value(s) = {Statements to execute},
          
       _ = { default_execution_statements }
   };
  */ 

   let marks = 98; 
   let grade = match marks {
   90..=100 =>  'A', 
   80..=89  =>  'B', 
   70..=79  =>  'C',
   60..=69  =>  'D',
   _ =>         'F',
   };
   println!("The grade achieved is {}",grade);

}
```
#### While Loop 
```rust

   fn main()
   {   
    // -------------------------------------------
    // 			Loops
    // 			- loops with no condition 
    //			- While loop 
    // -------------------------------------------
  
    /*
       loop {
           println!("This is an infinite loop");
       }
    */   
   
       /*     
       let my_number = 5; 
       println!("Guess my number which is between 1 and 20"); 
       let mut guess: bool = false; 
    
   
       while guess != true {
           let mut number = String::new();
           std::io::stdin()
           .read_line(&mut number)
           .expect("failed to read input.");
       let number: u8 = number.trim().parse().expect("invalid input");
       
       if my_number  == number {
           println!("You guessed the number correctly");
           guess = true;  
       } else {println!("Please try again");}
       }
       
    */ 
    
    /*
    println!("Enter a number and i will tell you the next 
            number after your number divisible by both 2 and 5");    
    
    let mut number = String::new();
    std::io::stdin()
    .read_line(&mut number)
    .expect("failed to read input.");
    
    let mut number: u8 = number.trim().parse().expect("invalid input"); 
    let mut divisible_by_2_5 = false; 
    
    while divisible_by_2_5 != true{
        number = number +1; // number +=1;
        if number %2 ==0 && number %5 == 0 {
            println!("The number after you number divisible by both 2 and 5 is {}", number);
            divisible_by_2_5 = true;  
        }
    }
    */
   
    println!("Enter a number and i will tell you the next 
    number after your number divisible by both 2 and 5");    

    let mut number = String::new();
    std::io::stdin()
    .read_line(&mut number)
    .expect("failed to read input.");
    let mut number: u8 = number.trim().parse().expect("invalid input"); 

    number = number +1; 
    while (number %2 ==0 && number %5 == 0)  != true{
        number = number +1; // number +=1 
  
    }
    println!("The number after you number divisible by both 2 and 5 is {}", number);
}
```
#### For Loops
```rust

   fn main()
   {   
    // -------------------------------------------
    // 			Loops
    // 			- For loop 
    //          	- Looping through elements using an immutable reference
    //          	- Looping through elements using a mutable reference
    // -------------------------------------------
  
       /*
       let mut some_vec = vec![45, 30, 85, 90, 41,39];  
       
       for i in 0..=5  {    // 0..=5
               println!("The {}th value in the vector is {}", i, some_vec[i]);
       }
       */ 
   
      /*
      let some_vec = vec![45, 30, 85, 90, 41,39]; 
      for i in some_vec {
           println!("{}", i);   
      }      
      println!("{:?}", some_vec);   
      */
      
      /*
      let some_vec = vec![45, 30, 85, 90, 41,39]; 
      for i in some_vec.iter() {    // &some_vec
       println!("{}", i);    
      }      
      println!("{:?}", some_vec);  
       
      */
   
      let mut some_vec = vec![45, 30, 85, 90, 41,39]; 
      for i in &mut some_vec.iter_mut() {    // or &mut some_vec
            *i += 5; 
            println!("{}", i);    
      }      
      println!("{:?}", some_vec);    
   
    }
   
   ```
   #### Break and Continue
   ```rust
    
   fn main()
   {       
    // -------------------------------------------
    // 			Break: for stopping a loop
    // 			Continue: for skipping the current iteration
    // -------------------------------------------
  
        /*
        let mut var = 100; 
        loop {  
            var = var - 1; 
            if var % 13 == 0 {
                break; 
            }   
        }
        println!("The highest number lesser than the given number
                 divisible by 13 is {}", var); 
    
        */
        /*
        let mut var = 0; 
        let mut count = 0; 
        loop {  
            var = var + 1;
            if var % 5 ==0 && var %3 == 0 {
                println!("\nThe number which is divisible by by both 3 and 5 = {} \n", var); 
                count = count +1; 
                if count == 3 {
                    break
                }   else 
                {continue}
            } 
            print!("{} ", var);    // Because of continue this line will not be printed

        }
        */
       
        
        
        let mut var = 0; 
        let mut count = 0; 
        let req_number:i32 =  loop {  
            var = var + 1;
            if var % 5 ==0 && var %3 == 0 {
                println!("\nThe number which is divisible by by both 3 and 5 = {} \n", var); 
                count = count +1; 

                if count == 3 {
                    break var;
                } else {
                    continue
                }
            }             
            print!("{} ", var); 
        };

        println!("the required third highest number divisible by both 3 and 5 is {}", req_number);
         
    }
   
   ```
