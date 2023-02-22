import java.util.*;
 class tempcal1 {
     int put() {
         Scanner kb = new Scanner(System.in);
       int choice=0;
         float p1 = 0;
         double p2 = 0;
         float c = 0f;
         int ch = 0;
         System.out.println("If you want to calculate temperature press 1 \n If you want to find distance between 2d and 3d coordinate press 2 ");
         choice=kb.nextInt();
         if(choice==1){
         System.out.println("If want your temp from celsius to fahrenheit press 1 \n If want your temp from celsius to kelvin press 2 \n if you want to know about Difference of celsius  press 3");
         ch = kb.nextInt();

         switch(ch) {
             case 1:
                 p2 = 32.00;
                 System.out.print("enter temp in celsius ");
                 c = kb.nextFloat();
                 if (p2 == 32.00) {
                     p1 = c * (9.0f / 5.0f) + 32.0f;
                 }
                 System.out.print(" celsius to fahrenheit: ");
                 System.out.print(p1 + "°F");
                 System.out.println("");
                 c = 0;

                 break;
             case 2:

                 System.out.print("enter temp in celsius ");
                 c = kb.nextFloat();
                 p1 = c + 273.15f;
                 System.out.print(p1 + "°K");
                 System.out.println("");
                 break;
             default:
                 if (ch == 3) {
                     int ch1 = 0;
                     System.out.println("difference fahrenheit press 1 ");
                     System.out.println("difference kelvin press 2: ");
                     ch1 = kb.nextInt();
                     p1 = 0;
                     switch (ch1) {

                         case 1:
                             System.out.println("enter temp in celsius ");
                             c = kb.nextFloat();
                             p1 = c * 1.8f;
                             System.out.println(p1 + "diff in fahrenheit ");
                             System.out.println("");
                             break;
                         case 2:
                             System.out.println("enter temp in celsius ");
                             c = kb.nextFloat();
                             p1 = c * 1.0f;
                             System.out.println(p1 + "diff in kelvin ");
                             System.out.println("");
                             break;

                         default:
                             System.out.println("sorry can't go further");
                     }
                 } else {
                     System.out.println("enter only 3 for difference");
                 }
         }
         }
         else if (choice==2) {
             System.out.println("The coordinate for 2D Enter 1 and The coordinate for 3D Enter 2");
             ch = kb.nextInt();
             switch(ch){
                 case 1:
                     System.out.println("Enter The coordinate x1 and x2");
                     double x1=kb.nextInt(),x2=kb.nextInt();
                     double x3=x2-x1;
                     System.out.println("Enter The coordinate y1 and y2");
                     double y1=kb.nextInt(),y2=kb.nextInt();
                     double y3=y2-y1;
                     double d=0;
                     d=Math.sqrt(Math.pow(x3,2)+Math.pow(y3,2));
                     System.out.println(d);
                     break;
                 case 2:
                     System.out.println("Enter The coordinate x1 and x2");
                     x1=kb.nextInt();x2=kb.nextInt();
                     x3=x2-x1;
                     System.out.println("Enter The coordinate y1 and y2");
                     y1=kb.nextInt();
                     y2=kb.nextInt();
                     y3=y2-y1;
                     System.out.println("Enter The coordinate z1 and z2");
                     double z1=kb.nextInt();
                     double z2=kb.nextInt();
                     double z3=z2-z1;
                      d=0;
                     d=Math.sqrt(Math.pow(x3,2)+Math.pow(y3,2)+Math.pow(z3,2));
                     System.out.println(d);
                     break;
                 default:
                     System.out.println("sorry Can't go further");
             }
         }
         else{
             System.out.println("The choice you have entered is invalid");
         }

         return put();
     }

     public static void main(String[]args){
          tempcal ob=new tempcal();
         ob.put();

     }
}











