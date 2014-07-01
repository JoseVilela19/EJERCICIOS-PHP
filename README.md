EJERCICIOS-PHP
==============
1.- Mira esta serie: 7, 6, 8, 4, 9, 2, 10, 0, 11, -2, ...
Cree una función que recibe dos enteros: x e y. Si alguno de ellos es 0 o negativo, o si son mayores que 255, la función debe devolver -1
De lo contrario, la función debe devolver la suma de los elementos X e Y de la serie.
Por ejemplo: Si la función recibe x = 1, y = 3, se debería devolver: 15 (Debido a que la suma de la primera, más el tercer argumento es 7 +8 = 15).. Si la función recibe x = 8, y = 9, es conveniente devolver 11. (Debido a que la suma de la octava más el elemento noveno es 0 11 = 11).
La función recibirá 2 enteros, y devuelve un entero.

<html>
    <head>
        <meta charset="UTF-8">
        <title></title>
    </head>
    <body>
        <?php
        echo("EJERCICIO.1");
        function serie($x,$y){
            $numeroimpar=7;
            $numeropar=8;
            $suma=0;
            $valordevuelto=-1;
            echo("SERIE: 7,6,8,4,9,2,10,0,11,-2......");
            if((($x>0)&&($y>0))&&(($x<255)&&($y<255))){
                
            if ($x > $y) {
        $recorrido = $x;
    } else {
        $recorrido = $y;
    }
    for($i = 1; $i <= $recorrido; $i++){
                $r=$i%2;
                if ($r == 0) {
                  $numeropar = $numeropar -2;
                  echo($numeropar);
                   if(($x == $i)||($y == $i)) {
                      $suma = $suma + $numeropar;
                   }
                } else {
                  $numeroimpar = $numeroimpar +1;
                  echo($numeroimpar);
                  if(($x == $i) ||($y == $i)) {
                  $suma = $suma + $numeroimpar;
                   }
                }
              echo("  ");
            }
            echo ($suma);
        }
         else {
          echo(-1);
         }
        } 

    serie(0,-2);
                
        ?>
    </body>
</html>
2. Mira esta serie: 2, 2, 4, 12, 48, ... la semilla de esta serie fue el número 2 Mira esta serie:. 3, 3, 6, 18, 72, ... la semilla de esta serie fue el número 3.
Cree una función que recibe dos enteros: x, y  y. Si alguno de ellos es 0 o negativo, o si son mayores que 255, la función debe devolver -1
La función debe devolver el elemento y de las series generadas por x.
Por ejemplo, si la serie recibe x = 3, y = 4, es conveniente devolver 72, porque 72 es el cuarto elemento de la serie generado cuando x = 3.
La función recibirá 2 enteros, y devuelve un entero.

<html>
    <head>
        <meta charset="UTF-8">
        <title></title>
    </head>
    <body>
        <?php
       echo("EJERCICIO.2");
                function serie1($x,$y){
                      echo("SERIE: 2, 2, 4, 12, 48, ...... semilla..");
                      echo("  :");
            if((($x>0)&&($y>0))&&(($x<255)&&($y<255))){
                echo($x);
                  echo(" ");
                  for($i = 1; $i <= $y; $i++){
                      $x=$x*$i;
                      echo($x);
                      echo(" ");
                       }
                          echo("valor devuelto");
                       echo($x);
                
            }
            else {
          echo(-1);
         }
                }
                
                   serie1(2,0);   
        ?>
    </body>
</html>
3. Mira esta serie: 60, 30, 20, 15, 12 ... la semilla de esta serie fue el número 60.
Cree una función que recibe dos enteros: x, y y. Si alguno de ellos es 0 o negativo, o si son mayores que 255, la función debe devolver -1.
La función debe devolver el elemento y de las series generadas por x.
Por ejemplo: Si la función recibe x = 60, y = 3, devolverá 20, porque el 20 es el elemento 3 º en la serie genera cuando x = 60.
La función recibirá 2 enteros, devuelve un valor de punto flotante.

<html>
    <head>
        <meta charset="UTF-8">
        <title></title>
    </head>
    <body>
        <?php
       echo("EJERCICIO3");
               echo("serie: 60, 30, 20, 15, 12 ... la semilla de esta serie fue el número 60.");
              
               function serie2($x,$y){
                     if((($x>0)&&($y>0))&&(($x<255)&&($y<255))){
                   for($i = 1; $i <= $y; $i++){
                       if($x%$i==0){
                           $d=$x/$i;
                           echo($d);
                       }
                       
                   }
               }
                 else {
          echo(-1);
         }
                         }

                serie2(60,6);
                
                       
               
        ?>
    </body>
</html>
4. Dadas dos cadenas S1 y S2. Eliminar en S1 todos esos caracteres que se presentan en S2. Devolver un S1 limpio con los caracteres eliminados. Cualquier carácter se elimina tanto en mayúsculas como en minúsculas.
Por ejemplo, dado:
S1 = "La vida es bella" S2 = "El santo"
La función debe devolver: "vidb".
La función recibirá 2 cadenas y devolver una cadena

<html>
    <head>
        <meta charset="UTF-8">
        <title></title>
    </head>
    <body>
        <?php
        
       echo("EJERCICIO4");
      
                function Comparar() {
                    
                    $cadena = "La vida es bella" ;
                    $frase="El santo";
                    for($i=0;$i<strlen($cadena);$i++) {
                            
                      if ($cadena{$i} != "") {
                        for($j=0;$j< strlen($frase);$j++) {
              
                      if ($frase{$j} != "") {
                      if(strtoupper($cadena{$i})==strtoupper($frase{$j}))
                      $cadena{$i}=null;
                      }
                    }
                      }
                    }
                     for($k=0;$k<$i;$k++) {
                         echo($cadena{$k});
                        
                     }
                }
                
               
                 
               Comparar();
               
        ?>
    </body>
</html>
5. Escriba una función para eliminar los duplicados de una matriz ordenada de enteros en una línea de código. (Usted puede usar tantas declaraciones como sea necesario, pero el código debe ser escrito en una sola línea).
Ejemplo:
Si la función recibe esta matriz: A = [-3, -2, 0, 0, 5, 7, 9, 11, 11, 25]
La función debe devolver: A = [-3, -2, 0, 5, 7, 9, 11, 25]
La función recibirá un arreglo de enteros, y devolver una matriz de enteros.

<html>
    <head>
        <meta charset="UTF-8">
        <title></title>
    </head>
    <body>
        <?php
   echo("EJERCICIO5");

$input = array (-3, -2, 0, 0, 5, 7, 9, 11, 11, 25);

$amaga=Comparars($input);
 print_r($amaga);
 print_r("holaaaaaa");
 print_r($input);
 
 function Comparars($input) {
     $result = array_unique($input);
     return $result;
 }
        ?>
    </body>
</html>
6. Dada una cadena, que contiene palabras y espacios (caracteres especiales), crear una función que devuelva una cadena con las palabras en un orden inverso.
Ejemplo:
Si la función recibe: "esta es una prueba", debe regresar: "prueba una es este".
Si se recibe una cadena vacía, una cadena vacía se debe devolver. Si sólo hay una palabra recibida, la misma palabra que se debe devolver.
La función recibirá una cadena y devolver una cadena.

<html>
    <head>
        <meta charset="UTF-8">
        <title></title>
    </head>
    <body>
        <?php
       
               echo("EJERCICIO6");
               $k=0;
                $cadena =  "esta es una prueba" ;
                   
                    for($i=0;$i<strlen($cadena);$i++) {
                            
                      if ($cadena{$i} == " ") {
                     $k++;
                    
                    }
                    }
                    
                   echo$k;
              
        $porciones = explode(" ", $cadena);
      
         
              for($i=0;$k>=$i;$k--) {
                         echo($porciones{$k});
                        echo(" ");
                     }

         ?>
    </body>
</html>
7. Dada una cadena que contiene letras (mayúsculas y minúsculas), números y caracteres especiales, devuelva la misma cadena en minúsculas.
Por ejemplo, si la función recibe:
"Nanito, QUÉ bien! Este es un texto de ejemplo, Lorem Ipsum, 2 CONVertido ".
La función debe devolver:
"nanito, qué bien! este es un texto de ejemplo, lorem ipsum, 2 convertido ".
La función debe considerar la conversión: Todos los caracteres de AZ, A, E, I, O, U y Ñ.Otros caracteres seguirán siendo los mismos.
Limitación: La conversión debe hacerse teniendo en cuenta los valores ASCII. Obviamente no se puede utilizar las funciones proporcionadas por el lenguaje (toLowercase (), Lowercase (), etc.) No se puede tener una gran sentencia switch de los casos para cada letra, o un montón de if / else.
Esta función recibirá una cadena y devuelve una cadena

<html>
    <head>
        <meta charset="UTF-8">
        <title></title>
    </head>
    <body>
        <?php
        echo("EJERCICIO7");
 

 $frase="Nanito, QUÉ bien! Este es un texto de ejemplo, Lorem Ipsum, 2 CONVertido ";

    for($i=0;$i<strlen($frase);$i++) {
                            
               
                    $valor=ord($frase{$i});
                    
                      if(($valor>29&&$valor<256)) {
                         if(($valor>64&&$valor<91)) {
                    $valor=$valor+32;
                      $frase{$i}=chr($valor);
                      if($frase{$i}==" ") 
                       echo("  ");
                      echo($frase{$i});
                      
                      $valor=0;
                      $frase{$i}=null;
                         }
                        
                       if(($valor<65)|| ($valor>91)){
                           if($frase{$i}==" ") 
                          echo("  "); 
                      echo($frase{$i});
                         
                             
                         
                      }
                      }
                      
                             
                     
    }
                      
                   $p="É";
                      echo(ord($p));
                      $p="é";
                      echo(ord($p));


        ?>
    </body>
</html>

8. Dada una cadena, busque el número de palabras que tiene por lo menos una "a" como caracteres (mayúsculos o minúsculos). No tener en cuenta las variaciones de carácter como á, à, etc .. sólo los sencillos "A" y cuenta "A".
Las palabras siempre están separadas por un espacio, una coma, un punto y coma o un punto.
Por ejemplo:
Si la función recibe: ". Ah, este es un texto de muestra, que da una lid de análisis" La función debe devolver 5, ya que cinco palabras tiene caracteres "a". (Ah, muestra, da, una, análisis).
La función recibirá una cadena y devolver un entero.
Limitaciones: No utilice el split (función), o similar.

<html>
    <head>
        <meta charset="UTF-8">
        <title></title>
    </head>
    <body>
        <?php
        $k=0;
        $cadena=". Aaah, este es un texto de muestraa, que da unaa lida de anáalisis" ;
       echo("EJERCICIO8");
        $bandera=0;
        $k=0;
        $c=0;
                  for($i=0;$i<strlen($cadena);$i++) {
                         
                     if($cadena{$i}==" "){
                     $c++;
                     if($c=1){
                     $bandera=0;
                     }
                 
                     
                     }
                     if((($cadena{$i}=="a")||($cadena{$i}=="A"))&&($bandera==0)){
                      $k++;
                     $bandera=1;
                     if($c>1){
                     $bandera=1;
                     }
                     }
                    }
                    echo("la cantidad de palabras que tiene a son");
                    echo($k);
                      
        ?>
    </body>
</html>
9. Dado un número entero positivo determinar si es la potencia de dos de otro número entero.
No empezar a programar, lea las limitaciones.
Por ejemplo:
Si la función recibe 25, debe devolver TRUE, porque 5 ^ 2 = 25 Si la función recibe 1, debe devolver TRUE, porque 1 ^ 2 = 1 Si la función recibe 16, debe devolver TRUE, porque 4 ^ 2 = 16 Si la función recibe 14, debería devolver FALSE.
Limitación: No es posible utilizar las funciones de raíz cuadrada (sqrt () o similar), potenciación (pow () o similar). Sólo se permiten las operaciones aritméticas básicas (suma, resta, multiplicación, división), y las operaciones lógicas.
La función recibe un número entero positivo mayor que 0, y debe devolver un valor booleano.

<html>
    <head>
        <meta charset="UTF-8">
        <title></title>
    </head>
    <body>
        <?php
       echo("EJERCICIO9");
     
                function calcular($valor){
                      $p=0;
                if($valor>0) {
                    for($i=1;$i<$valor;$i++) {
                    
                   $r=$i*$i;
                     if($r==$valor)
                         $p=$r;
                   
                }
                 if($p==$valor){
                 return true;}
                 else{
                return false;
                 }
                
                    
                }
                }
              if (calcular(16)==true) {
              echo("es correcto");}
                  else{
                     echo("es incorrecto");
                  }
                      
                
        ?>
    </body>
</html>
10. Un número perfecto es un número entero positivo que es igual a la suma de sus divisores apropiados. Por ejemplo, 6 es un número perfecto porque 6 = 1 +2 +3.
Crear una función que recibe dos valores X y Y, debe devolver  el menor número perfecto encontrado, que es mayor o igual que X y menor o igual a Y. Si ningún número perfecto encontró, debe devolver -1.
Por ejemplo, si la función recibe X = 5, Y = 7, se debe devolver 6, porque 6 es el número perfecto menor entre 5 y 7.
La función recibirá dos enteros y devolver un entero.

<html>
    <head>
        <meta charset="UTF-8">
        <title></title>
    </head>
    <body>
        <?php
       echo("EJERCICIO10");
              /* Este programa crea números perfectos en un rango dado. */
$x = 5; //número donde inica el rango
$y = 7; //número donde ternina el rango

for ( $prf=$x; $prf<=$y; $prf++ ) //ciclo que nos sirve para recorer el rango deseado
{
$c=0; // contador para almacenar los datos con residuo con valor de cero
for ($b=1; $b<$prf; $b++) //ciclo para efectuar la división desde el inicio hasta fin
{
$o=$prf%$b; //operación para obtener el residuo si es Cero
if ($o==0) //decisión si secumple
{
$c=$c+$b; //sumará a c su valor más el número que posee residuo cero
}
}
if ($c==$prf) //si c es igual al valor recorido en el primer ciclo entonces es perfecto
{
echo "$prf es un numero perfecto - "; // visualizar el número perfecto
}
}   
        ?>
    </body>
</html>
11. Dada una matriz de enteros, encontrar que se repite más veces. Devuelve el número que tiene más repeticiones. Si dos números tienen la misma cantidad de repeticiones, devuelva el número más bajo.
Por ejemplo, dada la matriz:
A = [1, 5, 3, -2, 4, 2, 4, -2, 5, 5, 2, 1, 3]
1 se repite 2 veces, 5 se repite 3 veces, 3 se repite 2 veces, 4 se repite 2 veces 2 se repite 2 veces
El número que más se repite es 5 La función debe devolver:.. 5 (5 Porque se repite 3 veces en la matriz).
La función recibirá una matriz de enteros y devolver un entero.

<html>
    <head>
        <meta charset="UTF-8">
        <title></title>
    </head>
    <body>
        <?php
       echo("EJERCICIO11");
             $A =array(1, 5, 3, -2, 4, 2, 4, -2, 5, 5, 2, 1, 3);  
             $tamaño=count($A) ;
            $c=0;
            $j=0;
            for($i=0;$i<$tamaño;$i++) {
            
              for($k=0;$k<$tamaño;$k++) {
            
                 if(($A{$k})==($A{$i})){
                 $c++;
            
                  }
            
              
               }
                if($c>$j){
                   $j=$c; 
                 $aux=$A{$i};
                }
                 $c=0;
            }
           
            echo($aux);
            echo($j);
            
            
           
        ?>
    </body>
</html>
12. Índice de equilibrio de una secuencia es un índice tal que la suma de los elementos en índices más bajos es igual a la suma de los elementos en los índices más altos.
Cree una función que recibe una matriz de enteros y devuelve el primer índice de equilibrio encontrado. Si no hay ningún índice de equilibrio encontrado, la función debe devolver -1
Por ejemplo, si la matriz recibida es: A = [-7, 1, 5, 2, -4, 3, 0]
3 es un índice de equilibrio, porque: a [0] + A [1] + A [2] = A [4] + A [5] + A [6]
En otras palabras, usted debe encontrar el índice de la matriz en la que la suma de los elementos de la izquierda es igual a la suma de los elementos adecuados.
En el ejemplo, la función devolverá 3, porque es el primer índice de equilibrio se encuentra en la matriz.
La función recibe un arreglo de enteros y devuelve un entero.

<html>
    <head>
        <meta charset="UTF-8">
        <title></title>
    </head>
    <body>
        <?php
       echo("EJERCICIO12");
                $A = array(-7, 1, 5, 2, -4, 3, 0);
                 $tamaño=count($A) ;
                 $total=0;
                         $total1=0;
                 $par=$tamaño%2;
                 if($par!=0);
                 $tamaño--;
                 $r=$tamaño/2;
                 echo($r);
                 
                  for($i=0;$i<$r;$i++) {
                      $total=$total+$A{$i};
                  }
                  $r++;
                  for($i=$r;$i<$tamaño;$i++) {
                      $total1=$total1+$A{$i};
                  }
                  echo($total);
                  echo($total1);
        ?>
    </body>
</html>

13. Se le da una matriz con números enteros positivos y negativos. Escriba una función para cambiar el orden de los elementos de la matriz de tal manera que los enteros negativos estén al principio, los enteros positivos queden al final. Cero (0) y números enteros que tienen el mismo signo no cambia el orden.
Por ejemplo, si la función recibe: a[0] = 4; a[1] = -3; a[2] = -100; a[3] = 7; a[4] = 0; a[5] = 1; a[6] = -6;
la función debe devolver:
a[0] = -3; a[1] = -100; a[2] = -6; a[3] = 4; a[4] = 7; a[5] = 0; a[6] = 1;
La función recibe un arreglo de enteros y devuelve un array de enteros.
Limitaciones: Usted no puede utilizar métodos proporcionados por el lenguaje de clasificación. (Por ejemplo, Array.sort (), sort (), etc ..). Si usted lo necesita, debe crear su propia implementación de la función de clasificación.

<html>
    <head>
        <meta charset="UTF-8">
        <title></title>
    </head>
    <body>
        <?php
       echo("EJERCICIO13");
                $input = array (4, -3, -100,7,0,1,-6);
$tamaño=count($input) ;
 print_r("holaaaaaa");
 print_r($input);
$aux=$input{0};
  for($k=0;$k<$tamaño;$k++) {
      
    for($j=0;$j<$tamaño;$j++) {
    if($input{$j}>$input{$k})
    {
        $aux=$input{$j};
        $input{$j}=$input{$k};
        $input{$k}=$aux;
    }
     
 }
     
 }
  for($k=0;$k<$tamaño;$k++) {
      echo($input{$k});
      echo(" ");
  }
 

        ?>
    </body>
</html>
14. Mira esta serie: 53, 35, 64, 46, 75, 57, 86 , 68, 97, 79, 108, 810, 119, 911, 1210, 1012, ... las semillas de esta serie fueron los números 5 y 3.
Mira esta serie: 103, 310, 114, 411, 125, 512, 136, 613, 147, 714, 158, 815, 169, 916, 1710, 1017, ... las semillas de esta serie fueron los números 10 y 3.
Mira esta serie: 1012, 1210, 1113, 1311, 1214, 1412, 1315, 1513, 1416, 1614, 1517, 1715, 1618, 1816, 1719, 1917, ... las semillas de esta serie fueron los números 10 y 12.
Cree una función que recibe tres enteros: x, y y z. Si alguno de ellos es 0 o negativo, o si son mayores que 255, la función debe devolver -1
La función debe devolver el elemento Z de la serie generada por x y y.
Por ejemplo: Si la función recibe x = 5, y = 3, z = 3, devolverá 64, porque 64 es el elemento 3 º en la serie generada cuando x = 5 e y = 3.
La función recibirá 3 enteros, devolver un entero.

<html>
    <head>
        <meta charset="UTF-8">
        <title></title>
    </head>
    <body>
        <?php
       echo("EJERCICIO14");
                $x=4;
                $y=5;
                $z=5;
                echo(" ");
                 for($k=0;$k<$z;$k++) {
                     $producto=$x*10;
                     $resultado=$producto+$y;
                     echo($resultado);
                    echo(" ");
                    if($k!=$z){
                    $producto=$y*10;
                     $resultado=$producto+$x;
                     $k++;
                     if($z%2!=0){
                         if($k==$z)
                             $resultado=null;
                     }
                         
                    echo($resultado);
                   
                    }
                    
                     $x++;
                     $y++;
                     echo("  ");
                 }
                
                
                
        ?>
    </body>
</html>
   <?php
        echo("EJERCICIO15");
        function  matriz($input){
       $tamaño=count($input) ;
       for($k=0;$k<1;$k++) {
           $indice{$k}=$input{$k};
           $suma=$suma+$input{$k};
       }
        for($k=2;$k<4;$k++) {
           $indice1{$k}=$input{$k};
            $suma1=$suma1+$input{$k};
       }
        for($k=0;$k<7;$k++) {
           $indice2{$k}=$input{$k};
            $suma2=$suma2+$input{$k};
       }
        }
        $suma3= $indice2{0};
        matriz(array (4, -3, 7, 2, 4, -5, 1, 2));
        ?>
