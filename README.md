# Pila-de-abecedario
package pilabec;

import java.util.Scanner;

public class Pila_abecedario {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        Scanner entrada=new Scanner (System.in);
        int op = 0;
        char tope='Z';
        
        
        do{
            
            System.out.println("1 - Llenar \n"
                    + "2 - Mostrar \n"
                    + "3 - Eliminar \n"
                    + "4 - Salir\n");
            //el menu
          switch(op= entrada.nextInt()){ //para introducir las opciones del menu
              case 1 :
                  if(tope>=op){
                    System.out.println("Valores agregados ");
                   //Se muestra el mensaje cuando se selecciona la opcion de llenar
                  }else{
                    System.out.println("La pila esta llena ");  
                    //Cuando ya se mostro el abecedario de la pila y se quiere meter una segunda vez de llenado mostrara este mensaje
                  }break;
              case 2 :
                  if(op==2 ){
                     for(char i='Z';i>='A';i--){   
                     //la variable i es igual a z para que este vaya decrementando de z..a 
                         System.out.println( i);   //para imprimir el abecedario de z..a
                     }
                  }else{
                     System.out.println("La pila esta vacia");
              //cuando se quiere mostrar antes de llenar se muestra este mensaje para
              //indicar que la pila aun no se llena
                 }break;
               case 3:
                  if(tope >=3){
                     
                     System.out.println("Letra eliminada....   " +tope--);
                       //para mostrar que elemento se elimina 
                       }
                      
                      else{
                      System.out.println("No hay elementos para eliminar");
                      //Cuando no se llena la pila en un principio se muestra el mensaje.
                      } break;          
        }
          
    }while(op!=4);
  }
}
