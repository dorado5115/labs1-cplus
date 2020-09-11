# labs1-cplus

# LABORATORIO DE ALGORITIMOS 

* Copyright (C) 2020 Geoffrey Porto <geoffrey.porto@tecmilenio.mx>
* Class: Fundaments of programming in C++ (c11)
* Date: 2020-08

## Definitions

### Variables 
* bool 
    
    Almacena el valor verdadero o falso.
* char 

    Normalmente un solo octeto (un byte). Este es un tipo entero.
* short: 
* int
    
    El tamaño más natural de entero para la máquina.
* long
    
    Variable largo
* float
    
    Un valor de punto flotante de precisión simple.
* doble
    
    Un valor de coma flotante de doble precisión.
* void
    
    Representa la ausencia de tipo.
* wchar_t
    
    Un tipo de carácter amplio.


### Operadores aritiméticos
Los operadores aritméticos se pueden utilizar para combinaciones apropiadas de estos tipos:				
* x + y // sumar, Agrega dos operandos A + B
* +x // incrementar, Operador de incremento, aumenta el valor entero en uno A++
* x − y // menos, Resta el segundo operando del primer A - B
* −x // decrementar, Operador de disminución, disminuye el valor entero en una A--
* x ∗ y // multiplicar, Multiplica ambos operandos A * B
* x / y // dividir, Divide el numerador por el numerador B / A
* x% y // resto (módulo) para enteros, Operador de módulo y el resto de después de una división entera

### Operadores de comparación
También pueden los operadores de comparación:
* x == y // igual
* x! = y // no es igual
* x <y // menor que
* x> y // mayor que
* x <= y // menor o igual x> = y // mayor o igual que

### Loops y bucles
Los ciclos repetitivos de ejecucion código.
* Loop "while"

    Repite una declaración o un grupo de declaraciones mientras una condición determinada es verdadera. Prueba la condición antes de ejecutar el cuerpo del bucle.

* Lopp "For"

    Ejecuta una secuencia de declaraciones varias veces y abrevia el código que administra la variable de ciclo.

* Lopp "do ... while"

    Como una declaración "while", excepto que prueba la condición al final del cuerpo del bucle.

* Loops anidados

    Puede utilizar uno o más bucles dentro de cualquier otro bucle "while", "for" o "do.. while".

### Declaraciones de Decisión (If, else, switch )
* declaración "If"

    Una declaración "si" consta de una expresión booleana seguida de una o más declaraciones.

* declaración "if ... else"

    Una instrucción "if" puede ir seguida de una instrucción "else" opcional, que se ejecuta cuando la expresión booleana es falsa.

* declaración "switch"

    Una declaración de "cambio" permite probar la igualdad de una variable con una lista de valores.

* declaraciones "if" anidadas

    Puede utilizar una declaración "si" o "más si" dentro de otra declaración "si" o "más si".

* declaraciones de "switch" anidadas

    Puede utilizar una declaración de "cambio" dentro de otra declaración de "cambio".

### Librerias base
Las librerias base más importantes de C++.
* iostream

    Este archivo define los objetos cin, cout, cerr y clog, que corresponden al flujo de entrada estándar, el flujo de salida estándar, el flujo de error estándar sin búfer y el flujo de error estándar con búfer, respectivamente.

* iomanip
    
    Este archivo declara servicios útiles para realizar E / S formateadas con los llamados manipuladores de flujo parametrizados, como setw y setprecision.

* fstream

    Este archivo declara servicios para el procesamiento de archivos controlado por el usuario. Lo discutiremos en detalle en el capítulo relacionado con archivos y secuencias.

### Markdown para Consola
* Shell:      console, Shell
* Bash:       bash, sh, zsh
* Powershell: powershell, ps
* Dos:        dos, bat, cmd

```{r, engine='zsh', count_lines}
   sudo your cmd
```


## Labs of Numbers

```cpp

/*+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
*  NOMBRE:  GEOFFREY PORTO                                    FECHA:              *
*  MATRICULA:                                                                     *
*  OBJETIVO: CALCULAR LA DISTANCIA ENTRE DOS PUNTOS USANDO TEOREAM DE PITAGORA    *
*  ENTRADA: LAS COORDENADAS DE LOS DOS PUNTOS (X1, Y1) y (X2 , Y2)                *
*  SALIDA: LA DISTANCIA ENTRE LOS DOS PUNTOS                                      *
*                                                                                 *
* ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++*/

#ifdef NUMEROS

#include <iostream>
using namespace std;
 
int main () {
   // Numeros
   short  s;
   int    i;
   long   l;
   float  f;
   double d;
   
   // Valores
   s = 10;      
   i = 100;    
   l = 100000; 
   f = 170.27;  
   d = 20741.957;
   
   // Mostrar los valores
   cout << "short  s :" << s<< "\n";
   cout << "int    i :" << i << "\n";
   cout << "long   l :" << l << "\n";
   cout << "float  f :" << f << "\n";
   cout << "double d :" << d << "\n";

   // operaciones mathematicas;
   cout << "sin(d) :" << sin(d) << "\n";
   cout << "abs(i)  :" << abs(i) << "\n";
   cout << "floor(d) :" << floor(d) << "\n";
   cout << "sqrt(f) :" << sqrt(f) << "\n";
   cout << "pow( d, 2) :" << pow(d, 2) << "\n";
 
   return 0;
}

#endif
```

## Labs of Class
Escribe los algoritmos para cada uno de los siguientes problemas:
* DISTANCIA: Calcular y desplegar la distancia que existe entre dos puntos dado que se proporcionan como dato de entrada los dos puntos (x1, y1) y (x2, y2).
* PARIMPAR: Determinar si el número dado como dato de entrada es “par” o “impar”  y Obtener y desplegar la suma de los impares de 1 a n donde n será dato de entrada.

```cpp
/*+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
*  NOMBRE:  GEOFFREY PORTO                                    FECHA:              *
*  MATRICULA:                                                                     *
*  OBJETIVO: CALCULAR LA DISTANCIA ENTRE DOS PUNTOS USANDO TEOREAM DE PITAGORA    *
*  ENTRADA: LAS COORDENADAS DE LOS DOS PUNTOS (X1, Y1) y (X2 , Y2)                *
*  SALIDA: LA DISTANCIA ENTRE LOS DOS PUNTOS                                      *
*                                                                                 *
* ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++*/

#ifdef DISTANCIA

#include <iostream>
using namespace std; //Refatorización el código para usar definición de espacio de trabajo

// para usar std::complex, std::real, std::imag 
#include <complex>
#include <cmath>
#include <iomanip>
   
float distancia(float, float, float, float);
   
int main() { 

    //Define variables de entrada y salida
    float x1, x2, y1, y2, distancia;

    //limpia pantalla
    system("clear");

    //imprimir titulo del programa
    cout <<"\n\nCalculo de la distancia entre dos puntos en el plano cartesiano. \n";
    
    //Solicitando del usuario los datos de entrada
    cout <<"\n\nIntroduzca las coordenadas del primer punto x1 y x2: \n";
    cin >> x1 >> x2;

    //Solicitando del usuario los datos de entrada
    cout <<"\nIntroduzca las coordenadas del segundo punto y1 y y2: \n";
    cin >> y1 >> y2;

    //Calculando la distancia
    distancia = sqrt((x1 - y1)*(x1 - y1 ) + (x2 - y2)*(x2 - y2));

    //Imprime al usuario los datos de salida
    cout <<"\nLa distancia entre los puntos x1("<<x1 <<"), y1("<<y1 <<") y x2("<<x2 <<"), y2("<<y2 <<") es : " <<distancia << "\n";

    return 0;
   
}

#endif

```
## Compilation and linking 
```{r, engine='zsh', count_lines}
   sudo g++ -DDISTANCIA nombre-equipo-lab1.cpp -o bin/distancia
```

```cpp

/*+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
*  NOMBRE:  GEOFFREY PORTO                                     FECHA:            *
*  MATRICULA:                                                                    *
*  OBJETIVO: CALCULAR EL PAR O IMPARR DE LOS NUMERO                              *
*  ENTRADA: NUMEROS ENTEROS                                                      *
*  SALIDA: MOSTRAR SI EL(OS) SON PAR O IMPAR                                     *
*  COMPILACIÓN: sudo g++ -DPARIMPAR class.cpp -o bin/parimpar                    *
* +++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++*/
   

#ifdef PARIMPAR

#include <iostream>
using namespace std; //Refatorización el código para usar definición de espacio de trabajo

// para usar std::complex, std::real, std::imag 
#include <complex>
#include <cmath>
#include <iomanip>
   
int main() { 
    
    //Define variables de entrada y salida
    int num;

    //Variables para calcular la cantidad de pares e impares
    int n, p=0,i=0,c=0,x;

    //limpia pantalla
    system("clear");

    //Solicitando del usuario los datos de entrada
    cout<<"Escriba un numero: ";
    cin>>num;

    //Comparando si el numero es par o impar, si las residuo de la división es ==0, entpnces es par, caso contrario es impar.
    if(num % 2 == 0){
        cout<<"El numero es Par\n";
    } else {
        cout<<"El numero es Impar\n";
    }
    
    
    //Solicitando del usuario los datos de entrada
    cout<<"Ingresar cantidad de numeros par e impares:";
    cin>>n;

    //Ejecutando el ciclo de hasta n veces
    while (c<n)
    {
        cout<<"Ingresar numero:";
        cin>>x;

        //Calularr la suma de numeros par e impar
        if(x % 2==0)
            p=p+1;
        else
            i=i+1;
            c=c+1;
    }

    //Imprime al usuario los datos de salida
    cout<<"los numeros pares son:"<<p<<endl;
    cout<<"los numeros impares son:"<<i<<endl;
}

#endif

```

## Compilation and linking 
```{r, engine='zsh', count_lines}
   sudo g++ -DPARIMPAR nombre-equipo-lab1.cpp -o bin/parimpar
```



## LABORATORIO DE ALGORITIMOS I

1. Crear algoritimo para obtener y despliega el área de un triángulo cuando el usuario proporciona como datos de entrada la base y la altura.
2. Crear algoritimo para determinr si el número dado por el usuario es “primo”, "negativo < -10 ",“positivo > 100 ” o “cero”.
3. Crear algoritimo para determinar el promedio de los números pares y el promedio de los números impares de una lista de valores enteros proporcionada por el usuario donde el último número es un cero.


```cpp

/*+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
*  NOMBRE:                                     FECHA:                               *
*  MATRICULA:                                                                       *
*  OBJETIVO: CALCULAR EL AREA DEL TRIANGULO                                         *
*                                                                                   *
*  ENTRADA:                                                                         *
*  SALIDA: MOSTRAR EL AREA DEL TRIANGULO                                            *
*  COMPILACIÓN: sudo g++ -DAREATRRINAGULO equipo-nombre-lab1.cpp -o bin/areatriangulo *
* ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++*/


#ifdef AREATRIANGULO
//Código aqui...

#endif

#ifdef NUMEROSPRIMONEGPOSCERO
//Código aqui...

#endif

#ifdef PROMEDIOSPARESIMPARES
//Código aqui...

#endif

```


## LABORATORIO DE ALGORITIMOS II

1. Crear algoritimo para determinar el área y volumen de un cilindro dado su radio (R) y altura (H).
2. Crear algoritimo para determinar el total a pagar por el cliente en una tienda que ofrece descuentos por temporada dependiendo del total comprado:
    * Si la compra es menor a 300 pesos, el descuento es del 5%.
    * Si la compra es de 301 a 1000 pesos, el descuento es del 15%.
    * Si la compra es mayor a 1000 pesos el descuento es del 25%.
3. Para un estudio meteorológico se registra el promedio de temperatura diaria. Con base en los registros de 15 dias, se debe obtener la siguiente información:
    * La mayor temperatura de la quincena y el día en el que ocurrió.
    * La menor temperatura de la quincena y el día en el que ocurrió.
    * La temperatura promedio de la quincena.
    * La temperatura promedio de la primera semana del mes.
    * La temperatura promedio de la segunda semana del mes.


```cpp

/*+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
*  NOMBRE:                                     FECHA:                               *
*  MATRICULA:                                                                       *
*  OBJETIVO: CALCULAR LA AREA Y VOLUMEN DEL CILINDRO                                *
*  ENTRADA:                                                                         *
*  SALIDA: MOSTRAR EL AREA Y VOLUMEN DEL CILINDRO                                   *
*  COMPILACIÓN: sudo g++ -DAREAVOLCILINDRO equipo-nombre-lab2.cpp -o bin/areavolcilindro *
* ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++*/


#ifdef AREAVOLCILINDRO
//Agrega tu Código aqui...

#endif


/*+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
*  NOMBRE:                                     FECHA:                               *
*  MATRICULA:                                                                       *
*  OBJETIVO: CALCULAR EL TOTAL A PAGAR DEL CLIENTE                                  *
*  ENTRADA:                                                                         *
*  SALIDA: MOSTRAR EL TOTAL A PAGAR DEL CLIENTE                                     *
*  COMPILACIÓN: sudo g++ -DTOTALAPAGAR equipo-nombre-lab2.cpp -o bin/totalapagar    *
* ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++*/

#ifdef TOTALAPAGAR
//Agrega tu Código aqui...

#endif


/*+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
*  NOMBRE:                                     FECHA:                               *
*  MATRICULA:                                                                       *
*  OBJETIVO: CALCULAR DATOS METEOROLOGICOS                                          *
*  ENTRADA:                                                                         *
*  SALIDA: MOSTRAR LOS DATOS METEOROLOGICOS                                         *
*  COMPILACIÓN: sudo g++ -DMETEOROLOGIA equipo-nombre-lab2.cpp -o bin/meteorologia  *
* ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++*/
#ifdef METEOROLOGIA
//Agrega tu Código aqui...

#endif

```