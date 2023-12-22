# project_00
TypeScript Calculator Tutorial | Calculator in TypeScript with Inquirer |Project00_calculator


import inquirer from "inquirer"

const answer :{
    num1 :number ,
    num2 :number ,
    operator : string
} = await inquirer.prompt([
    {
        type : 'number',
        name : 'num1',
        message :' Kindly enter your first number'
    },
    {
        type : 'number',
        name : 'num2',
        message :' Kindly enter your second number'
    },
    { type : 'list',
    name : 'operator',
    message :' Kindly enter your operator',
    choices :[ 'add' , 'subtract', 'divide', 'multiply']}
])

if( answer.operator === 'add'){
    console.log(answer.num1 + answer.num2);
    
} else if( answer.operator === 'subtract'){
    console.log(answer.num1 - answer.num2);
    
} else if( answer.operator === 'divide'){
    console.log(answer.num1 / answer.num2);
    
} else if( answer.operator === 'multiply'){
    console.log(answer.num1 * answer.num2);
    
}
