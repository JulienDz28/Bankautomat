import java.util.Scanner;

public class main {


    public static void main(String args[]) {

        begruessungText();




    }

    public static boolean abfrageKonto(int a){


            if(a == 22004){
                return true;
            }else{
                System.out.println("Falsche Kundennummer.");
                return false;
            }

    }

    public static void begruessungText(){
        Scanner sc = new Scanner(System.in);
        System.out.print("Hallo, herzlich willkommen! Bitte geben Sie Ihre Kundennummer an: ");
        int knummer =  sc.nextInt();
        abfrageKonto(knummer);
        if(abfrageKonto(knummer) == true) {

            System.out.print("Bitte geben Sie nun Ihren Pin an: ");
            int pin = sc.nextInt();
        } else{
            System.out.println("Die Kundennummer war leider falsch. Bitte versuchen Sie es erneut.");
            begruessungText();
        }


    }


}

