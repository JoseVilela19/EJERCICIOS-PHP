EJERCICIOS-PHP
==============
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
