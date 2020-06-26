# Programa 2

## Hecho por Ballinas Arteaga Jesus Emilio

##Programa 2: 
imprime en pantalla los cuadrados de los primero 10 números naturales: 1,4,9,25, etc.

### Como ingresar los numeros
En este programa automaticamente te dara los primero 10 números naturales: 1,4,9,25, etc...

### Que es un compilador?

En informática, un compilador es un tipo de traductor que transforma un programa entero de un lenguaje de programación a otro.​ Usualmente el lenguaje objetivo es código máquina, aunque también puede ser traducido a un código intermedio o a texto.

### Estructura

- CG.h
- Simple.lex
- SM.h
- ST.h
- Simple.y

### Como iniciar ?

1. Clona el repositorio de github
2. Crea una rama alterna dentro del repositorio con: 

            git checkout -b nombre_de_tu_rama

3. Dentro de la ruta del proyecto abre la terminal de comandos e ingresa lo siguiente:

            make

4. Para probar el ejecutable tienes que ingresar el siguiente comando:

            make probar

### Comandos del Make

- make: Ejecuta todos los procesos de compilacion y analisis lexico dentro de los documentos.
- clean: Limpia los elementos creados del producto de la compilacion y flexeado.
- probar: Con este lanzamos el comando de prueba.

## Que hay de nuevo en este programa

En este programa podemos ver que acepta las variables de true y false, que son las variables boolaneas que se utilizan para declarar si algo es verdadero o falso, por otro lado se incertaron para que acepte lo valores reales, ademas de una ligera modificacion para que pueda adquirir arreglos unidimensionales con limite estatico.

# Archivos modificados

## Simple.lex

            38  bool		{ return(BOOL); }
            39  true	    { yylval.boolval = true;
		                        return(TRUE); }
            41  false	    { yylval.boolval = false;
		                        return(FALSE); }
## Simple.y

            68  bool boolval;  
            83  %token INTEGER FLOAT READ BOOL WRITE LET IN
            */ Intento de arreglo unidimensional
            | '[' exp ',' exp ',' exp ']'
            */ Declaracion de variables boolaneas
	        | TRUE			{ gen_code( LD_INT, $1 ); }
	        | FALSE 		{ gen_code( LD_INT, $1 ); }