# Exercise-14
Counting Vowels

/*
*Jonathan Saldivar
*ITSE 1302-011
*Exercise 14
*Class thas counts all the Vowels in a sentence
*/

package com.LowerCaseVowelCounter;
import java.util.Scanner;

public class LowerCaseVowelCounter {

private int intACounter = 0;
private int intECounter = 0;
private int intICounter = 0;
private int intOCounter = 0;
private int intUCounter = 0;

   private String strInput = "";
   private Scanner objInput = new Scanner(System.in);
   public LowerCaseVowelCounter(){
   UserInput();
 }
   
    private String UserInput() {
    System.out.println("Type in a sentence to find out how many vowels are used.");
    System.out.println("Begin: ");
    
    strInput = objInput.next();
    VowelCounter();
    return strInput;
}
    
   private void VowelCounter(){
   for(int intIndex = 0;
   intIndex < strInput.length(); intIndex++) {
    
   switch (strInput.charAt(intIndex)) {
    
   case 'a':
   intACounter++;
   break;
    
   case 'e':
   intECounter++;
   break;
    
   case 'i':
   intICounter++;
   break;
    
   case 'o':
   intOCounter++;
   break;
   
   case 'u'
   intUCounter++;
   break;
    
  }
  
 }
    PrintVowelCounter();
}
   
   private void PrintVowelCounter(){
   System.out.println("Your vowel count is for a is: " + intACounter);
   System.out.println("Your vowel count is for e is: " + intECounter);
   System.out.println("Your vowel count is for i is: " + intICounter);
   System.out.println("Your vowel count is for o is: " + intOCounter);
   System.out.println("Your vowel count is for u is: " + intUCounter);
    
   resetCounters();
    
}
    
    
   private void resetCounters(){
   intACounter = 0;
   intECounter = 0;
   intICounter = 0;
   intOCounter = 0;
   intUCounter = 0;
   UserInput();
    
   }
}
