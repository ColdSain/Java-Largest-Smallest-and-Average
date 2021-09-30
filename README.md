# Java-Largest-Smallest-and-Average
 A code that makes you entera list of 10 random numbers and will automatically tell you the largest, smallest, and the average of the list.

import java.util.Scanner;
import java.util.ArrayList; 

    public class CSlab4{
        
        public static void main(String[] args){
            
            ArrayList<Integer> list1 = new ArrayList<>();
            Scanner input = new Scanner(System.in);
            
            int num1 = 0; 
            
            System.out.println("Enter 10 numbers that are between 1 and 100."
                    + "I will tell you the smallest, largest, and avarage.");
            
            do
            { 
                int num2 = input.nextInt(); 
                
                if (num2 < 1)
                {
                    System.out.println("Number is out of range, try again.");
                }
                else if (num2 > 100)
                {
                    System.out.println("Number is out of range, try again.");
                }
                else
                {
                    list1.add(num2); 
                    num1++;    
                }
                
            } while (num1 !=10);
            
            int smal = list1.get(0); 
            int larg = list1.get(0); 
            double avg = 0; 
            
            for (int i = 0; i <list1.size(); i++)
            {
                if (list1.get(i) > larg)
                {
                    larg = list1.get(i); 
                }
            }
            
            for (int i = 0; i <list1.size(); i++)
            {
                if (list1.get(i) < smal)
                {
                    smal = list1.get(i); 
                }
            }
            
            for (int i = 0; i < list1.size(); i++)
            {
                avg = avg + list1.get(i); 
            }
            avg = avg /10; 
            
            System.out.println("Smallest: " + smal);
            System.out.println("Largest: " + larg); 
            System.out.println("Average: " + avg);
            
        }
    } 
