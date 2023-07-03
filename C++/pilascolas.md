
Agregar el método size() a la clase MyQueue para obtener el número de elementos en la cola.
```C++
int size(){
    int count = 0;
    Node* tmp = root;
    while(tmp!=NULL){
        count++;
        tmp = tmp->get_next();
    }
     return count;
 }
```
AgrImplementegar el método printInverted() de MyQueue para imprimir los elementos en orden inverso.

Agregar el método clear() a la clase MyQueue para eliminar todos los elementos de la cola.

Modificar el método dequeue() de MyQueue para devolver -1 si la cola está vacía

Agregar el método peek() a la clase MyQueue para obtener el valor del primer elemento sin eliminarlo.

Agregar el método size() a la clase MyStack para obtener el número de elementos en la pila.

Agregar el método printInverted() de MyStack para imprimir los elementos en orden inverso.

Agregar el método clear() a la clase MyStack para eliminar todos los elementos de la pila.

Modificar el método pop() de MyStack para devolver -1 si la pila está vacía

Agregar el método peek() a la clase MyStack para obtener el valor del elemento superior sin eliminarlo.

Implementar un método reverse() en la clase MyQueue que invierta el orden de los elementos en la cola sin utilizar estructuras de datos adicionales.

Modificar la clase MyQueue para agregar un método removeDuplicates() que elimine los elementos duplicados en la cola, dejando solo una instancia de cada elemento.

Implementar un método interleave() en la clase MyQueue que tome dos colas y cree una nueva cola intercalando los elementos de ambas colas.

Modificar la clase MyQueue para agregar un método rotate(int k) que rote los elementos de la cola k posiciones hacia la izquierda.

Modificar la clase MyStack para agregar un método sort() que ordene los elementos en la pila de forma ascendente.

Modificar la clase MyStack para agregar un método getMin() que devuelva el elemento mínimo en la pila.

Modificar la clase MyStack para agregar un método reverseK(int k) que invierta los elementos de la pila en grupos de tamaño k.

Generar 4 nuevos ejercicios tipo examen con chatGPT
Resolverlos sin usar chatGPT
Resolverlos usando chatGPT y comparar respuestas indicando diferencias.
