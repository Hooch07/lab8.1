# lab8.1
echo "# lab8.1" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/Hooch07/lab8.1.git
git push -u origin master

/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package lab8;

/**
 *
 * @author X00135191
 */
import java.util.Scanner;
public class Lab8 {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        
        double length1, length2, length3, height, radius;
        double result;
        int option = 0;
        String repeat = "Y";
        
        while(repeat.equalsIgnoreCase("Y")){
        System.out.println("Calculation of volume for solid objects");
        System.out.printf("1. Cube Volume \n"
                         + "2. Cylinder Volume \n"
                         + "3. Sphere Volume \n"
                         + "4. Exit \n"
                         + "Your Choice: ");
                 
        option = in.nextInt();
                
        switch(option){
            case 1:
                System.out.println("Cube Calculation");
                System.out.println("Please enter 3 lengths for a cube");
                length1 = in.nextDouble();
                length2 = in.nextDouble();
                length3 = in.nextDouble();
                result = length1*length2*length3;
                System.out.println("The volume of the cube is "+ result);
            break;
            case 2:
                System.out.println("Clyinder Calculation"); 
                System.out.println("Please enter the radius of the cylinder");
                radius = in.nextDouble();
                System.out.println("Please enter the height of the cylinder");
                height = in.nextDouble();
                result = Math.PI * (radius*radius) * height;
                System.out.println("The volume of the cylinder is "+ result);
                break;
            case 3:
                System.out.println("Sphere Calculation");
                System.out.println("Please enter the radius of the sphere");
                radius = in.nextDouble();
                result = (4.0 / 3.0) * Math.PI * (radius*radius*radius);
                System.out.println("The volume of the sphere is "+result);
                break;
            case 4:
                System.out.println("You have selected to exiit the program ");
                        System.exit(0);
                break;
            default: 
                    System.err.println("Error");
    }  
            System.out.println("Enter Y to run again");
            repeat = in.next();
  }   
}
}
