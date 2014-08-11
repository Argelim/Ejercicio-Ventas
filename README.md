Ejercicio-Ventas
================

import java.util.Scanner;

public class Main {
	static int iphone_totales, ipad_totales, smartphone_totales, tablet_totales, ingresos_totales, ganancias;
	
	public static void main(String[] args) {
		Scanner entrada = new Scanner(System.in);
		
		//variables
		int iphone, ipad, smartphone, tablet;
		iphone = 699;
		ipad = 449;
		smartphone = 249;
		tablet = 59;
		boolean salir = false;
		
		//Recibir datos por teclado
		while(salir == false)
			{
			System.out.println("Indique el numero del articulo vendido, para calcular su salario pulse 5");
			System.out.println("	1. Iphone \n	2. Ipad \n	3. Smartphone \n	4. Tablet \n");
			int articulo = entrada.nextInt();
			
			switch (articulo)
			{
			case 1:
			{
				System.out.println("¿Cuantos Iphone has vendido?");
				int n1 = entrada.nextInt();
				iphone_totales = n1 * iphone;
				break;
			}
			case 2:
			{
				System.out.println("¿Cuantos Ipad has vendido?");
				int n2 = entrada.nextInt();
				ipad_totales = n2 * ipad;
				break;
			}
			case 3:
			{
				System.out.println("¿Cuantos Smartphone has vendido?");
				int n3 = entrada.nextInt();
				smartphone_totales = n3 * smartphone;
				break;
			}
			case 4:
			{
				System.out.println("¿Cuantas Tablets has vendido?");
				int n4 = entrada.nextInt();
				tablet_totales = n4 * tablet;
				break;
			}
			case 5:
				
				salir = true;
			}
			}
		ingresos_totales = iphone_totales + ipad_totales + smartphone_totales + tablet_totales;
		ganancias = 200 + (9 * ingresos_totales / 100);
		System.out.println("Los ingresos totales son de: " + ingresos_totales + "Euros\n");
		System.out.println("Las ganancias este mes ascienden a: " + ganancias + "Euros \n");
	}

}
