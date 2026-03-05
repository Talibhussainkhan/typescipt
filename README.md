# typescipt
// union = In TypeScript, a union type allows a variable, function parameter, or return 
// type to hold more than one type of value, effectively acting as an "OR" (|) operator. 

type id = string | number
function abc ( a : id){
    console.log(a)
}

// intersection = In TypeScript, an intersection (&) type combines multiple types 
// into one, requiring an object or value to possess all properties/characteristics of 
// every constituent type.

type Person = {
    name : String
};

type Employee = {
  employeeId : Number
}

type staff = Person & Employee

const user : staff = {
name : 'talib',
employeeId : 12
}

// Type Narrowing = TS can narrow a broad type to a specific one inside a block:
function proccess(val : string | number) {
    if (typeof val === "string") {
    console.log(val.toUpperCase()); // TS knows it's a string here
  } else {
    console.log(val.toFixed(2)); // TS knows it's a number here
  }
}

// Generics = Write reusable code that works with any type while staying type-safe:

function first <T>(arr : T[]) : T{
    return arr[0]
}

first(['abc', 'xyz', 'asda'])



