# new-project
#Test Case 1
@Test
public void fizzBuzzConvertorLeavesNormalNumbersAlone(){

    FizzBuzzConverter fizzBuzz = new FizzBuzzConverter();

    Assert.assertEquals("1", fizzBuzz.convert(1));
    Assert.assertEquals("2", fizzBuzz.convert(2));
}

#Test case 2
@Test
public void fizzBuzzConvertorMultiplesOfThree(){

    FizzBuzzConverter fizzBuzz = new FizzBuzzConverter();

    Assert.assertEquals("Fizz", fizzBuzz.convert(3));
}
#condition for number 3
if(toConvertToFizzBuzz%3==0){
   return "Fizz";
}

#Test case 3
@Test
public void fizzBuzzConvertorMultiplesOfFive(){

    FizzBuzzConverter fizzBuzz = new FizzBuzzConverter();

    Assert.assertEquals("Buzz", fizzBuzz.convert(5));
}
#condition for number 5
if(toConvertToFizzBuzz%5==0){
   return "Buzz";
}
#finally the convert method for 3 and 5
public String convert(int toConvertToFizzBuzz) {

    if(toConvertToFizzBuzz%5==0){
       return "Buzz";
    }
    
    if(toConvertToFizzBuzz%3==0){
       return "Fizz";
    }
    
    return String.valueOf(toConvertToFizzBuzz);
}
#Test case 4
@Test
public void multiplesOfBothThreeAndFive(){
   FizzBuzzConverter fizzBuzz = new FizzBuzzConverter();

   Assert.assertEquals("FizzBuzz", fizzBuzz.convert(15));
}
#test method
public String convert(int toConvertToFizzBuzz) {

    if(toConvertToFizzBuzz%15==0){
       return "FizzBuzz";
    }
    
    if(toConvertToFizzBuzz%5==0){
        return "Buzz";
    }
    
    if(toConvertToFizzBuzz%3==0){
        return "Fizz";
    }
    
    return String.valueOf(toConvertToFizzBuzz);
}
#finally actual method
@Test
public void outputTheHundredFizzBuzzes(){

   FizzBuzzConverter fizzBuzz = new FizzBuzzConverter();
    for(int i=1; i<=100; i++){
       System.out.println(fizzBuzz.convert(i));
    }
}
