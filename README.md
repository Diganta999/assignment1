### Ans to the question no 3


##  Explain the difference between any, unknown, and never types in TypeScript. 
- Any Data Type : 

Any is a data type in TypeScript . Any type is used when we deal with third party programs ,
 also expect any variable but we do not know the exact type of variable .

- example :  

         let input : any;
         
         input=10;
         input='diganta'
         input= true

-Unknown : 

unknown is a type in TypeScript . Any value can be assigned to a variable of type unknown .
you can not directly access property .


- example: 

         let data :unknown;

         data= 'hello';
         data = true;

- Never Type :

Never is  type in TypeScript . when you are sure that something is never going to occur.
never always  return Error .

- example: 
       

       function showError(message:string):never{
        throw new Error(message);
       }



### Ans to the question no 7 


## Provide an example of using union and intersection types in TypeScript.


- Union : Union is a keyword in TypeScript . A union type means a value can be one type or another .
We use union types when a value could be multiple possible types like user input.

- example :

      function inputData(input: string | number){
          console.log(input)
        }

      inputData('Data');
      inputData(123);


- Intersection : Intersection is a keyword in Type script . An intersection type means a value must have all the properties from multiple types.
when we use intersection types we want to merge multiple types into one.




- example :

          type Data1 = {
            name:string;
            roll: number;
          }
          type Data2 ={
            age:number;
            school:string;
          }

          type Person = Data1 & Data2 ;

          const diganta: Person = {
            name:'Diganta Sikder',
            roll: 1 ,
            age: 19 ,
            school: 'Balibabla Adarsha High School'

          }


