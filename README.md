# labs1-cplus

#LABORATORIO DE ALGORITIMOS 

Copyright (C) 2020 Geoffrey Porto <geoffrey.porto@tecmilenio.mx>
Class: fundaments of C++ (c11)

## Definitions

### Variables 
bool: almacena el valor verdadero o falso.
char: normalmente un solo octeto (un byte). Este es un tipo entero.
int: El tamaño más natural de entero para la máquina.
float: un valor de punto flotante de precisión simple.
doble: un valor de coma flotante de doble precisión.
void: Representa la ausencia de tipo.
wchar_t: un tipo de carácter amplio.

### Operadores aritiméticos
Los operadores aritméticos se pueden utilizar para combinaciones apropiadas de estos tipos:				
* x + y // sumar
* +x // incrementar
* x − y // menos
* −x // decrementar
* x ∗ y // multiplicar
* x / y // dividir
* x% y // resto (módulo) para enteros

### Operadores de comparación
También pueden los operadores de comparación:
* x == y // igual
* x! = y // no es igual
* x <y // menor que
* x> y // mayor que
* x <= y // menor o igual x> = y // mayor o igual que


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