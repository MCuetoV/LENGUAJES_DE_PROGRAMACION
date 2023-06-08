Escribir una función que intercambie el valor de dos variables enteras utilizando punteros.
```C++
#include <iostream>
using namespace std;
void intercambiarVal(int* a, int* b){
    int tmp = *a;
    *a = *b;
    *b = tmp;
}
int main(){
    int a = 10;
    int b = 20;

    cout<<"Valor de a: "<<a<<endl;
    cout<<"Valor de b: "<<b<<endl;
    intercambiarVal(&a, &b);
    cout<<"Nuevo valor de a: "<<a<<endl;
    cout<<"Nuevo valor de b: "<<b<<endl;
    return 0;
}
```
Escribir una función que reciba un puntero a un número entero y verifique si es par.
```C++
#include <iostream>
using namespace std;
void esPar(int* ptr){
    if(*ptr % 2 ==0){
        cout<<"Es par."<<endl;
    }
    else{
        cout<<"Es impar."<<endl;
    }
}
int main(){
    int n;
    cout<<"Ingresar numero: "<<endl;
    cin>>n;
    esPar(&n);

    return 0;
}
```
Escribir una función que reciba un puntero a un número entero y determine si es positivo, negativo o cero.
```C++
#include <iostream>
using namespace std;
void tipodesigno(int* ptr){
    if(*ptr<0){
        cout<<"El numero es negativo"<<endl;
    }
    else if(*ptr==0){
        cout<<"El numero es cero"<<endl;
    }
    else{
        cout<<"El numero es positivo"<<endl;
    }
}
int main(){
    int n;
    cout<<"Ingresa numero: "<<endl;
    cin>>n;
    tipodesigno(&n);
    return 0;
}
```
Escribir una función que reciba un arreglo de enteros y su tamaño, y retorne el valor máximo utilizando punteros.
```C++
#include <iostream>
using namespace std;
    int mayorvalor(int* arr, int tamanio){
    int mayor = *arr; // inicia con mayor en posicion 0
    for(int i = 1; i<tamanio; i++){ // recorre el resto
        if(*(arr+i) > mayor){
            mayor = *(arr + i); // si encuentra uno mayor actualiza
        }
    }
    return mayor;
}
int main(){
    int tamanio;
    cout<<"Ingresar tamanio de array: "<<endl;
    cin>>tamanio;

    int* arr = new int[tamanio];

    cout<<"Ingresar elementos: "<<endl;
    for(int i=0;i<tamanio;i++){
        cin>>*(arr+i);
    }
    cout<<"El mayor valor es: "<<mayorvalor(arr, tamanio);
    return 0;
}
```
Escribir una función que reciba un puntero a un arreglo de caracteres y lo imprima en reversa. \0 representa null
```C++
#include <iostream>
using namespace std;
void inversaarray(int* arr, int tamanio){
    int* inicio = arr; // inicia y declara puntero al comienzo
    int* fin = arr + tamanio-1; // inicia y declara puntero al final

    while(inicio<fin){ //mientras que el puntero inicio este antes del puntero fin(al medio)
        int tmp = *inicio; // intercambia valores del inicio(pos 0) y final(pos tamanio-1)
        *inicio = *fin;
        *fin = tmp;

        inicio++; //mover puntero inicio al siguiente
        fin--; //mover puntero fin al anterior
    }
int main(){
    int tamanio; // Ingresa tamanio y elementos igual que ejercicio anterior
    cout<<"Ingresar tamanio de array: "<<endl;
    cin>>tamanio;
    int* arr = new int[tamanio];
    cout<<"Ingresar elementos: "<<endl;
    for(int i=0;i<tamanio;i++){
        cin>>*(arr+i);
    }

    inversaarray(arr, tamanio);
    cout<<"La inversa del array es: "<<endl;
    for(int i=0;i<tamanio;i++){
        cout<<*(arr+i)<<" ";
    }
}
```
Escribir un programa que:
a) Implemente una funcion que reciba un valor entero "n", lea "n" valores desde el teclado y los retorne en un array.
b) Implemente una funcion que reciba un array (como un puntero a entero), un valor "n" con la longitud e imprima los valores en pantalla.
c) La misma función anterior pero recorriendo el arreglo de otra forma.
```C++
#include <iostream>
using namespace std;
int* crearArreglo(int n){
    // crear arreglo de punteros de tamano n
    int* arreglo = new int[n];
    // recorrer arreglo
    for(int i=0; i<n;i++){
        // para cada posicion existe un valor que es ingresado por usuario en cada posicion i
        int valor;
        cout<<"Ingrese valor a la posicion "<< i <<":"<<endl;
        cin>>valor;
        arreglo[i] = valor;
    }
    return arreglo;
}
void imprimir(int* arreglo, int tamanio){
    cout<<"Los valores del arreglo son: ";
    for(int i =0;i<tamanio;i++){
        cout<<arreglo[i]<<" ";
    }
}

void imprimirPtr(int* arreglo, int tamanio){
    int* ptr = arreglo;
    cout<<"Los valores de arreglo son: ";
    for(int i=0; i<tamanio; i++){
        cout<<*ptr<<" "; // si se pusiera ptr mostraria direccion de memoria
        ptr++; //el siguiente sino repetira el mismo
    }
}

int main(){
    int n;
    cout<<"Ingrese tamano de arreglo: "<<endl;
    cin>>n;
    int* valores = crearArreglo(n);

    //imprimir(valores, n);

    imprimirPtr(valores, n);

    return 0;
}
```


