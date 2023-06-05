1.-Declara una variable entera llamada "edad" y asígnale el valor 25. Imprime el valor de la variable en la consola. b) Declara una variable de tipo caracter llamada "letra" y asígnale el valor 'A'. Imprime la letra en la consola.
```C++
#include <iostream>
using namespace std;
int main(){
    int edad = 25;
    char letra = 'A';
    cout<<edad<<endl;
    cout<<letra<<endl;
}
```
2.-Solicitar un caracer y determinar si es mayúscula o minúscula: a) usando isupper, islower, b) sin usar dichas funciones
```C++
#include <iostream>
using namespace std;
int main(){
    char c;
    cout<<"Ingresa letra: "<<endl;
    cin>>c;
    if(isupper(c))
        cout<<"La letra es mayuscula"<<endl;
    else if(islower(c))
        cout<<"La letra es minuscula"<<endl;
    else
        cout<<"No es letra"<<endl;
  
    // ASCII
    // 65('A') - 90('Z')
    // 97('a') - 122('z')
    char d;
    cout<<"Ingresa una letra: "<<endl;
    cin>>d;
    if(d>='A'&& d<='Z')
        cout<<"Es mayuscula"<<endl;
    else if(d>='a'&&d<='z')
        cout<<"Es minuscula"<<endl;
    else
        cout<<"No es letra";
}
```
3.-Imprime los números del 1 al 10 utilizando un bucle "for".
```C++
#include <iostream>
using namespace std;
int main(){
    // Loop for simple
    for(int i=1; i<=10; i++){
        cout<<i<<" ";
    }
    cout<<endl;
}
```
4.-Imprime los números pares del 1 al 20 utilizando un bucle "while".
```C++
#include <iostream>
using namespace std;
int main(){
    while(number<=20){
        if(number % 2 == 0){
            cout<<number<<" ";
        }
        number++;
    }
    cout<<endl;
}
```
5.-Imprime los números impares del 10 al 1 utilizando un bucle "do while.
```C++
#include <iostream>
using namespace std;
int main(){
    int num = 10;
    do
    {
        for(num; num>=1;num--){
            if(num % 2 != 0){
                cout<<num<<" ";
            }
        }
    } while (num>=1);
    cout<<endl;
}
```
6.-Lee un número del usuario e imprime "Par" si es divisible por 2, "Impar" si no lo es.
```C++
#include <iostream>
using namespace std;
int main(){
    int numer;
    cout<<"Ingresar numero: "<<endl;
    cin>>numer;
    if(numer % 2 ==0){
        cout<<"PAR"<<endl;
    }
    else
        cout<<"IMPAR"<<endl;
}
```
7.-Lee un número del usuario y utiliza un switch para imprimir el día de la semana correspondiente.
```C++
#include <iostream>
using namespace std;
int main(){

}
```
8.-Declara un array de enteros llamado "numeros" de tamaño 5. Asigna los valores del 1 al 5 a cada posición del array. Imprime los elementos del array en la consola.
```C++
#include <iostream>
using namespace std;
int main(){
    int dia;
    cout<<"Ingresar numero del 1 al 7 para ver que dia de la semana corresponde: "<<endl;
    cin>>dia;
    switch (dia)
    {
    case 1:
        cout<<"Lunes";
        break;
    case 2:
        cout<<"Martes";
        break;
    case 3:
        cout<<"Miercoles";
        break;
    case 4:
        cout<<"Jueves";
        break;
    case 5:
        cout<<"Viernes";
        break;
    case 6:
        cout<<"Sabado";
        break;
    case 7:
        cout<<"Domingo";
        break;
    default:
        cout<<"No valido";
        break;
    }
    cout<<endl;
}
```
9.-Lee 5 números enteros del usuario y almacénalos en un array llamado "numeros". Luego, calcula y muestra la suma de los números.
```C++
#include <iostream>
using namespace std;
int main(){
    int numeros[5];
    int suma = 0;
    
    for(int i = 0; i<5; i++){
        cout<<"Ingrese numero: "<<endl;
        cin>>numeros[i];
    }
    for(int i = 0; i<5;i++){
        suma = suma + numeros[i];
    }
    cout<<"La suma de los numeros ingresados es: "<<suma<<endl;
}
```
10.-Declara una estructura llamada "Persona" con dos miembros: "nombre" (cadena de caracteres) y "edad" (entero). Crea una variable de tipo "Persona" y asígnale valores. Imprime los valores en la consola.
```C++
#include <iostream>
using namespace std;
struct Persona{
    string nombre;
    int edad;
};
int main(){
    Persona superheroe;
    superheroe.nombre = "Chapulin Colorado";
    superheroe.edad = 50;
    
    cout<<superheroe.nombre<<endl;
    cout<<superheroe.edad;
}
```
11.-Declara una estructura llamada "Punto" con dos miembros: "x" y "y", ambos enteros. Crea una variable de tipo "Punto" y pide al usuario que ingrese los valores de "x" y "y". Imprime los valores en la consola.
```C++
#include <iostream>
using namespace std;

struct Punto{
    int x;
    int y;
};

int main(){
    Punto punto;
    cout<<"Ingresar coordenada x:"<<endl;
    cin>>punto.x;
    cout<<"Ingresar coordenada y:"<<endl;
    cin>>punto.y;

    cout<<"X: "<<punto.x<<endl;
    cout<<"Y: "<<punto.y<<endl;
}
```
12.-Declara una variable de tipo "float" llamada "precio" y asígnale el valor 9.99. Imprime el valor de la variable con 2 decimales en la consola.
```C++
#include <iostream>
using namespace std;
int main(){
    float precio = 9.99;
    cout<<precio;
}
```
13.-Imprime los números del 10 al 1 en orden descendente utilizando un bucle "for".
```C++
#include <iostream>
using namespace std;
int main(){
    for(int i = 10; i>=1; i--){
        cout<<i<<" ";
    } nm
}
```
14.-Calcula la suma de los números del 1 al 100 utilizando un bucle "while". Imprime el resultado.
```C++
#include <iostream>
using namespace std;
int main(){
    int numero = 1;
    int suma = 0;
    
    while(numero<=100){
        suma = suma + numero;
        numero++;
    }
    cout<<suma;
}
```
15.-Imprime la tabla de multiplicar del 5 utilizando un bucle "do while".
```C++
#include <iostream>
using namespace std;
int main(){
    int num = 0;
    int tabla;
    do
    {
        tabla = num*5;
        cout<<"5x"<<num<<"="<<tabla<<endl;
        num++;
    }while(num<=10);
    cout<<endl;
}
```
16.-Lee un carácter del usuario y utiliza un switch para determinar si es una vocal (a, e, i, o, u) o una consonante. Usar: tolower para convertir a minúsculas.
```C++
#include <iostream>
using namespace std;
int main(){

}
```
17.-Lee un número del usuario y utiliza un switch para imprimir el nombre del mes correspondiente.
```C++
#include <iostream>
using namespace std;
int main(){

}
```
18.-Declara un array de caracteres llamado "palabra" de tamaño 10. Lee una palabra del usuario y almacénala en el array. Imprime la palabra en la consola.
```C++
#include <iostream>
using namespace std;
int main(){

}
```
19.-Lee 5 números enteros del usuario y almacénalos en un array llamado "numeros". Luego, encuentra el número mayor en el array y muéstralo en la consola.
```C++
#include <iostream>
using namespace std;
int main(){

}
```
20.-Declara una estructura llamada "Rectangulo" con dos miembros: "largo" y "ancho", ambos enteros. Crea una variable de tipo "Rectangulo" y pide al usuario que ingrese los valores de "largo" y "ancho". Calcula y muestra el área del rectángulo.
```C++
#include <iostream>
using namespace std;
int main(){

}
```
