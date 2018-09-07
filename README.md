# TexasInstrument
import java.util.*;
import java.text.DecimalFormat;

public class TexasInsturments
{
	private static DecimalFormat df6 = new DecimalFormat(".######");
	private static Scanner scan;
	public static void main(String[] args) 
	{
		scan = new Scanner(System.in);
		System.out.println ("--------------------------------------------");
		System.out.println ("\tTexas Instruments Calculator"); //Title
		System.out.println ("--------------------------------------------");
		
		//Calculate the distance
        System.out.print ("\tInput first x coordinate: "); //Inputs (creating variables)
        double x1 = scan.nextDouble ();
        System.out.print ("\tInput first y coordinate: ");
        double y1 = scan.nextDouble ();
        System.out.print ("\tInput second x coordinate: ");
        double x2 = scan.nextDouble ();
        System.out.print ("\tInput second y coordinate: ");
        double y2 = scan.nextDouble ();
        
        //Math calculations 
        double xdif = Math.pow ((x2-x1), 2); //squaring (x2-x1)
        double ydif = Math.pow ((y2-y1), 2); //squaring (y2-y2);
        double total = Math.sqrt (xdif + ydif); //square root of  (x2-x2) + (y2-y1)
        
        System.out.println ();
        System.out.println ("\tDistance: " + df6.format(total));
        System.out.println ("--------------------------------------------");
        
      //==================================================================================================
        
      //Calculating Surface area and Volume
        System.out.println ();
        System.out.println ("\tWould you like to calculate");
        System.out.println ("\tthe volume and surface area");
        System.out.println ("\tof a sphere? (yes/no)");
        		  
        String a = scan.next(); // assigning the answer a variable
        
        if (a.equalsIgnoreCase("yes")) //if the person types yes this code shows up
        {
        	System.out.println ();
        	System.out.print ("\tInput radius: "); 
        	double radius = scan.nextDouble (); //Assigning variable to the radius
        	double volume = (4.0/3 * Math.PI * Math.pow(radius, 3)); // Calculating volume (But i can't figure out how to make 4/3 not 1)
        	double area = (4 * Math.PI * Math.pow(radius, 2)); // Calculating area
            
        	System.out.println ();
        	System.out.println ("\tSurface area = " + df6.format(area)); //Output
            System.out.println ("\tVolume = " + df6.format(volume)); 
        	
        }
        
        else if(a.equalsIgnoreCase("no")) //if they type no this shows up
        	System.out.println(""
        			+ "\tThank you");
        
        }

}
