# POO--Metodos-de-ordenamiento
Main Insercion
package OrdenarInsercion;

public class Main {

	public static void main(String[] args) {
		int arreglo[]= {5,11,13,15,4,12,23,3,4,2,1,45,13};
		
		OrdenarInsercion o= new OrdenarInsercion();
		o.Ordenar(arreglo);
		
		for(int i=0; i<arreglo.length;i++) {
			System.out.println(arreglo[i]);
		}

	}

}

ORDENAMIENTO INSERCION
package OrdenarInsercion;

public class OrdenarInsercion {

	public void Ordenar(int[] array) {
		
		int aux;
		int cont1,cont2;

		for(cont1 = 1; cont1 < array.length; cont1++) {
			aux= array[cont1];
			
			for(cont2 = cont1-1; cont2>=0 && array[cont2] > aux; cont2--) {
				array[cont2+1]=array[cont2];
				array[cont2] = aux;
			}
		}
	}

}
