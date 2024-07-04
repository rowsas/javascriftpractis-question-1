 
 //Q1

  function fullName(firstName,lastName){
    let fullName=firstName+ " " + lastName
    console.log(fullName)
 }

 fullName("moahmed","riskan") 
 +

 //Q2

 /* let poem= "The quote 'There is no exercise better for the heart than reaching down and lifting people up.' by John Holmes teaches us to help one another."

 console.log(poem); */


 //Q3

  /* let num="1 1 1 1 1\n2 1 2 4 8\n3 1 3 9 27\n4 1 4 16 64\n5 1 5 25 125"

 console.log(num) 
  */
 //Q4

 /* let rees="There is a commonly stated “rule” of grammar that beginning a sentence with and, or any other conjunction, is a mistake. But this is just not true. This supposed “rule” has no basis in actual writing, and even formal writing features plenty of sentences that start with and and other conjunctions. And we think that is really cool."
 let and= (rees.match(/\band\b/gi) || []).length;
 console.log(and); */

 //Q5

/*var year= new Date();
var birthYear = year.getFullYear();
console.log(birthYear);



var date1 = new Date();
var month = date1.getMonth() + 1; 
console.log(month);

var date2 = new Date();
var date = date2.getDate(); 
console.log(date);


var date3 = new Date();
var day = date3.getDay(); 
console.log(day); */



//Q6



/* function line(slope,slope2){
   this.slope,
   this.slope2,
}

 */


//Q8




const hours = prompt("Enter hours:");
  const perHour = prompt("Enter Rate Per Hour:");
  const weeklyearnings = hours * perHour;
  alert(`Your weekly earning is ${weeklyearnings}`);



  //Q9
  const currentyear = new Date().getFullYear();
  const birthyear = prompt("Enter your birth year:");
  const age = currentyear-birthyear;
  if(age >= 18){
     alert(`You are:${age}. You are old enough to drive.`);
  }else{
     const wait = 18- age;
  alert(`You are:${age}. You will be allowed to drive after${wait} years.`);
  }


  //10

  const numbers = [1,2,3,4,5,6,7];
  const evenNumbers = numbers.filter(function(number){
   return number%2===0;
  });
  console.log("Even Numbers:",evenNumbers);



  const NumBers = [1,2,3,4,5];
  const squareNumbers = NumBers.map(function(number ){
   return number * number;
  });
  console.log("Square Numbers:",squareNumbers);




  // 11
  const NumBers = [1,2,3,4,5];
  const squareNumbers = NumBers.map(function(number ){
   return number * number;
  });
  console.log("Square Numbers:",squareNumbers);
  


  // Q12

  
  //filer method 

  const books = [ 
   {
    title: "To Kill a Mockingbird",
    author: "Harper Lee", 
    genre: "Fiction",
    pages: 336, 
    publication_year: 1925, 
   }, 
   { 
   title: "1984", 
   author: "George Orwell",
   genre: "Dystopian",
   pages: 328, 
   publication_year: 1949,
    }, 
   {
    title: "Pride and Prejudice", 
    author: "Jane Austen",
    genre: "Romance",
    pages: 432, 
    publication_year: 1813,
    }, 
   {
    title: "The Great Gatsby",
    author: "F. Scott Fitzgerald", 
    genre: "Classic", 
    pages: 180,
 publication_year: 1925,
 },
 ]; 

const filterbookbypage = books.filter((books) =>{return books.pages >100;},{});
console.log(filterbookbypage);


const filterbookbypage1= books.filter((books) =>{return books.pages < 200;},{});
console.log(filterbookbypage1);

const  genreofFiction = books.filter((books) =>{return books.genre  ==="Fiction";},{});
console.log(genreofFiction);
//map method

const titles = books.map((books) => {return books.title;});
console.log(titles);

const author = books.map((books) => {return books.author;});
console.log(author);

const titlesauthor = books.map((books) => {return books.author;});
console.log(titlesauthor);

//raduce
const totalNumber = books.reduce((sum,books) => {return sum + parseInt(books.pages);},0);
console.log("total number of pages is " + totalNumber);

const totalNumberBypublication = books.reduce((result,books) => {
   if(typeof result[books.publication_year] === "undefined") {
      result[books.publication_year] = 1;
   }
   else { result[books.publication_year] +=1;}
   return result;
},{});
console.log(totalNumberBypublication);

//Q13 Arrow function 
const greets = name => {
   return `Welcome ${name} to the team.`;
 };
 
 console.log(greets('Ran')); // "Welcome Ran to the team."
 console.log(greets('Sara')); // "Welcome Sara to the team."

 //Q14 arrow funtion um math.floor useing
 const litres = time => {
   return Math.floor(time * 0.5);
 };
 
 console.log(litres(0)); // 0
 console.log(litres(2)); // 1
 console.log(litres(1.4)); // 0

 //Q15 reduce using and if condiction, arrow funtion
 const positiveSum = arr => {
   return arr.reduce((acc, num) => {
     if (num > 0) {
       return acc + num;
     } else {
       return acc;
     }
   }, 0);
 };
 
 console.log(positiveSum([1, 2, 3, 4, 5])); // 15
 console.log(positiveSum([1, -2, 3, 4, 5])); // 13
 console.log(positiveSum([-1, 2, 3, 4, -5])); // 9
 console.log(positiveSum([-1, -2, -3, -4, -5])); // 0
 console.log(positiveSum([])); // 0

 