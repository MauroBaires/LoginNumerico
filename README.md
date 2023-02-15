# LoginNumerico
Loggin numerico con tres intentos
package clasesiete;

import java.util.Scanner;

public class ejercicioUno {

	public static void main(String[] args) {
		// TODO Auto-generated method stub

		// EJERCICIO NUMERO 1
		//quiero hacer un programa de entrada segura
		// tengo un usuario y una clave predefinida usuario = admin clave = 123456
		// tiene oportunidad de equivocarse hasta 3 veces, despues de eso 
		// sale del sistema y no permine ingresar mas clave y usuario.
		int times = 0;
		int pin = 123456;
		int resto= 3;
		Scanner entrada = new Scanner(System.in);
		
		
			do {
				System.out.println("Bienvenido Usuario, ingrese la contraseña : ");
				int pass = entrada.nextInt();
				
				if (pass == pin) {  System.out.println("Password correcto, Bienvenido usuario");
				times = 3;
				
				}else {System.out.println("Contraseña incorrecta, intentelo " + (--resto) + " veces mas"); 
				times = times + 1;
						
				if (times ==3) System.out.println("Acceso reestringido, comuniquese con el administrador");
				}
			} while (times < 3);  
			
	 
	}

}
