package Proyecto;

import java.util.Scanner;

public class SemanaTres {
	
	
	public static void firstExercise() {
		   
    	Scanner scanner = new Scanner(System.in);

        System.out.print("Introduce el número del año: ");
        int anho = scanner.nextInt();


        int sigloActual = siglo(anho);
        int primerAnhoDelSiglo = primer_anho(sigloActual);

        System.out.println("El año " + anho + " pertenece al siglo " + sigloActual);
        System.out.println("El primer año del siglo " + sigloActual + " es: " + primerAnhoDelSiglo);

    }
	
    public static int siglo(int anho) {

        return (anho % 100 == 0) ? anho / 100 : (anho / 100) + 1;
    }

    public static int primer_anho(int siglo) {
        return (siglo - 1) * 100 + 1;
    }
    
    
    public static void secondExercise() {
    	Scanner scanner = new Scanner(System.in);

        System.out.print(" Ingresar la cantidad dinero en moneda local: ");
        int localCurrency = scanner.nextInt();


        int conversionAlas8AM = conversionAlas8AM(localCurrency);
        int conversionAlMediodia = conversionAlMediodia(localCurrency);

        System.out.println("Dinero en moneda local a las 8:00 Am es: " + conversionAlas8AM);
        System.out.println("Dinero en moneda local al Medio día es: " + conversionAlMediodia);

    }
    
    public static int conversionAlas8AM(int localCurrency) {
    	return localCurrency;
    }
    
    public static int conversionAlMediodia(int localCurrency) {
    	int discount = localCurrency * 10 / 100;
    	return localCurrency - discount;
    }
    
    
    public static void thirdExercise() {
    	Scanner scanner = new Scanner(System.in);

        System.out.print(" Ingresar la medida (Metros) del objeto: ");
        int meters = scanner.nextInt();
        
        double feet = meters * 3.28084;
        double inches = meters * 39.3701;
        int centimeters = meters * 100;
        

        System.out.println("El objeto mide: " + meters + " Metros");
        System.out.println("El objeto mide: " + feet + " Pies");
        System.out.println("El objeto mide: " + inches + " Pulgadas");
        System.out.println("El objeto mide: " + centimeters + " Centimetros");

    }

    public static void main(String[] args) {
     
    	Scanner scanner = new Scanner(System.in);
    	
    	/*Todos los metodos comienzan con la instancia de Scanner para la lectura
    	 * del teclado
    	 * 
    	 * El primer metodo consiste en la llamada al metodo siglo que nos retorna la 
    	 * información de a que siglo pertenece el año que se ingresa, despues hace el
    	 * llamado al metodo primer año para devolvernos el primer año del siglo que retorno
    	 * la funcion anterior.
    	*/
    	
    	firstExercise();
    	
    	
    	
    	
    	/* El segundo metodo consiste en ingresar el dato de la moneda local a convertir
    	 * usando el primer metodo de conversionALas8 nos devuelve el valor de la moneda local
    	 * en el horario de las 8AM y en el segundo metodo nos devolveria el valor de la 
    	 * moneda local en el horario del medio dia con un descuento del 10%, finalmente la funcion 
    	 * nos devolvera el valor de la moneda local a las 8AM y al medio dia.
    	*/
    	secondExercise();
    	
    	
    	/* En el tercer metodo se ingresa el metraje de un objeto y nos devolvera las medidas
    	 * del objeto en centrimetros, pulgadas y pies y para esto se crearon 3 variables que 
    	 * convierten la medida en metros del objeto y las convierte en cada una de las medidas necesarias.
    	*/
    	thirdExercise();
    	
        scanner.close();

    }
}
