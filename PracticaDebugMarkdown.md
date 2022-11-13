>#### ¿Qué hacen estas dos líneas de código?  
>string2= string2.substring(0, string2.length()-1);  
>string2=string2+"1";  
		
En la primera linea lo que pasa es que se substrae a la cadena una de sus posiciones al hacer el (.length()-1), pero luego se lo devuelve al sumarle 1 a un string, ya que cuando sumas un numero a un string lo unico que pasa es que se añade ese valor como si estuvieran juntando palabras.

>#### ¿Por qué no va el ==? ¿Qué tengo que hacer para solucionarlo ?  
>if(string1 == string2 ) {  
			System.out.println("SON IGUALES " + a);  
		}  
		else {  
			System.out.println("SON DIFERENTES");  
		}
		
El "==" lo que hace es comprobar si los objetos se encuentran en el mismo espacio de memoria, en cambio si deberia utilizar en ese caso el ".equals()" que lo que hace es comparar los valores de cada objeto.

>#### ¿Cómo hago la llamada para que funcione?
>public void funcion2() {  
>System.out.println("--------------------");  
>System.out.println("Esta es la función 2");  
>System.out.println("Cómo hago la llamada para que funcione????");  
>}

Para llamar a esta funcion, primero deberiamos convertirlo en un static, ya que ya esta dentro de una función principal, una vez llamamos convertimos esta funcion en static ya solo quedaria iniciarlo cuando nosotros queramos introduciendo el nombre de la funcion con sus parantesis, en este caso seria "funcion2()".

> #### Esta función no me va ... ¿ por que ? Tengo dos soluciones .. ¿como?  
>public static void main(String[] args) {  
		// TODO Auto-generated method stub  
		int a = 3;  
		int i;  
		for(i = 0; i<10; i++)  
			a *= i;  
		System.out.println("El valor de a es: "+a);  
		funcion1();  
		//Esta función no me va ... ¿ por que ?  
		// Tengo dos soluciones .. ¿como?  
		// funcion2();  
	}
	
No va porque el resultado siempre va ser igual a 0, ya que la int "i" tiene un valor inicial a 0, entonces cualquier cosa multiplicado por 0 da = 0, al principio del bucle la primera operacion es (a= a * i), que visto de otra manera es (a= 3*0), esto da un valor de 0, y luego va ir multiplicando numeros por 0 hasta llegar a 9, dando todos el mismo resultado de 0. Las maneras que yo veo de arreglarlo es simplemente al inicio del bucle, ponerle a "i" un valor inicial de 1 en vez de 0.
		
