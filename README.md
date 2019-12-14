# Assignment2
/question 1
use std::io;

fn calculation()->String{

    let mut value = String::new();

    io::stdin().read_line(&mut val)
    .expect("Failed to read line");

    val
}

fn main(){
    let numbers = "0123456789";
    let operator = ['+','-','*','/','^'];
     let values = Vec::new();

    loop{

        let input = calculation();
        let mut sign = String::new();
        let mut num1 = String::new();
        let mut num2 = String::new();

        let mut check = false;

        for i in input.chars(){
            for j in operations.iter(){
                if i == *j{
                    sign.push(i);
                    break
                }
            }
        }

        if &usr_input[0..1]=="0"{
            println!("bye");
            break;
        }

        for a in usr_input.chars(){  
            if a.to_string() == sign{
                check =true;
            }
            for b in nums.chars(){
                if a==b{
                    if check{
                        num2.push_str(&a.to_string());
                    }
                    else{
                    num1.push_str(&a.to_string());
                    }
                }
            }
        }



        let x= (num1.to_string()).parse::<f32>().expect("please provide valid input");
        let y= (num2.to_string()).parse::<f32>().expect("please provide valid input");
        // println!("{}",sign);

        if sign =="+"{
            println!("{}",x+y);
        }
        else if sign =="-"{
            println!("{}",x-y);
        }
        else if sign =="*"{
            println!("{}",x*y);
        }
        else if sign =="/"{
            println!("{}",x/y);
        }
        else if sign =="^"{
            println!("{}", f32::powf(x,y));
        }

    }

}
/question 2
use std::io;

struct Child{

    name:String,
    age:u8

}

trait primaryEducation{
    fn isPrimEdu(&self)->String;
}

trait bilingual{
    fn isbilingual(&self)->String;
}

impl primaryEducation for Child{
    fn isPrimEdu(&self)->String{
        format!("{}'s primary education is completed",self.name)
    }
}

impl bilingual for Child{

    fn isbilingual(&self)->String{
        format!("{} is bilingual",self.name)
    }

}


fn adoption<T:primEdu +bilingual>(child1: T, child2: T){

    println!("these children fulfil your requirements:\n{} and {}\n{} and {}",
    child1.isPrimEdu(),child1.isbilingual(),child2.isPrimEdu(),child2.isbilingual());
}

fn main(){

    let asad= Child{
        name:String::from("asad"),
        age :9
    };

    let hiba = Child{
        name :String::from("hiba"),
        age:8
    };

    adoptn(asad,hiba);
}


/question 5

1 - we can save them in a variable and then use them
2 - pass them as arguments to other functions.
3 - Create the closure in one place and then call the closure to evaluate it in a different context.
4--Closures can capture values from the scope in which they’re defined. 







