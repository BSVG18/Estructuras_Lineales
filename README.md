# Estructuras_Lineales

package javaapplication1;

import java.util.Scanner;

public class Pilas {
    
public static void main(String[] args) {

        Scanner Suma = new Scanner(System.in);
        
        int Tamaño = 0, Menu = 0, PilaC = 0;
        
        int Increment = 0, Increment2 = 0;
        System.out.print("Ingresa el tamaño de la pilas: ");
        int tam = Suma.nextInt();
        int[] PilaA = new int[Tamaño = tam];
        int[] PilaB = new int[Tamaño = tam];
        System.out.println("");
        do {
            System.out.println("1 - llenar pilas A, B.\n"
                    + "2 - mostrar pilas A,B.\n"
                    + "3 - vaciar pilas A,B.\n"
                    + "4 - unir pilar.\n"
                    + "5 - mostrar pila C.\n"
                    + "6 - salir.\n");

            System.out.print("seleccione una opción: ");

            switch (Menu = Suma.nextInt()) {
                case 1: 
                    for (int i = 0; i < Tamaño; i++) {
                        int numeros = (int) (Math.random() * (100) + (1)); //Generar números randoms del 1 al 100.
                        PilaA[i] = numeros;
                    }
                    for (int f = 0; f <= Tamaño; f++) { 
                        Increment++;//Incrementa un valor hasta que la variable f llegue al tamaño que el usuario ingreso.
                    }
                    for (int i = 0; i < Tamaño; i++) {
                        int numeros = (int) (Math.random() * (101) + (100)); //Generar números randoms del 100 al 200.
                        PilaB[i] = numeros;
                    }
                    for (int z = 0; z <= Tamaño; z++) {
                        Increment2++;//Incrementa un valor hasta que la variable z llegue al tamaño que el usuario ingreso.
                    }
                    System.out.println("Pila A y B llenas\n");
                    if (PilaC > 0){ //Si el usuario ya habia realizado la suma de las dos pila, se eleminaran cuando se ingrese nuevos valores a las pilas.
                            for (int j = 0; j < PilaC; j--) { 
                            PilaC--; 
                          }           
                        }
                    break;

                case 2: 
                    if (Increment > 0 && Increment2 > 0) { 
                        System.out.println("\nPila A");
                        for (int f = 0; f < Tamaño; f++) { //Mostrara los valores de la pila A.
                            System.out.print(PilaA[f]+"  "); 
                        }
                        System.out.println("\n\nPila B ");
                        for (int z = 0; z < Tamaño; z++) { //Mostrara los valores de la pila B.
                            System.out.print(PilaB[z]+"  "); 
                        }
                        System.out.println("\n");
                    } else {
                        System.out.println("No hay valores en las pilas a y b...\n"); //Se cumplira el "else" si no hay ningún valor en las pilas.
                    }
                    break;
                case 3: 
                    if (Increment > 0 && Increment2 > 0) { 
                        for (int i = 0; i <= Tamaño; i++) {
                            Increment--; Increment2--; //Se eleminaran los valores de las pilas A y B.
                            }
                        System.out.println("Pilas eliminadas \n");

                    } else {
                        System.out.println("No hay valores en las pilas a y b para eliminar... \n"); //Se cumplira el "else" si no hay ningún valor en las pilas.
                    }
                    break;
                case 4: 
                    if (Increment > 0 && Increment2 > 0) { 
                        System.out.println("Pilas sumadas...");
                        for (int f = 0; f < Tamaño; f++) {
                            PilaC = (PilaA[f]+PilaB[f]); //Se sumaran las pilas A y B y se almaceneran en la pila C.
                        }
                        System.out.println("");
                    } else {
                        System.out.println("No se han creado las pilas para unirlas... \n"); //Se cumplira el "else" si no se han sumado las pilas.
                    }
                    break;
                case 5: 
                    if (Increment > 0 && Increment2 > 0) { 
                        System.out.println("\nPila C");
                        if (PilaC > 0) { //Si sa se sumaron las pilas A y B entonces se cumple la condición.
                            for (int f = 0; f < Tamaño; f++) {
                                System.out.print(PilaA[f]+PilaB[f]+"  "); //Se mostrara los valores de la Pila C.
                            }
                            System.out.println("\n");
                        }else{ 
                            System.out.println("No se han sumado las pilas a y b\n"); //No se mostraran los valores de la Pila C sino se suman las pilas a y b.
                        }
                    } else {
                        System.out.println("No se a creado la pila c \n");//Si aun no existen las pilas a y b no podra existir la pila c.                                            
                    }
                    break;
            }
        } while (Menu != 6); 
    }
}
