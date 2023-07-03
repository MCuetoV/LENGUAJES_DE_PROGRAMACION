
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
```C++
    void printReversa(Node* node) {
        if (node == NULL) {
            return;
        }
        printReversa(node->get_next());
        cout << node->get_value() << "->";
    }

    void printInverted() {
        cout << "Cola al reves: ";
        printReversa(root);
        cout <<"NULL"<<endl;
    }
```
Agregar el método clear() a la clase MyQueue para eliminar todos los elementos de la cola.
```C++
    void clear() {
        Node* tmp = root;
        while (tmp != NULL) {
            Node* next = tmp->get_next();
            delete tmp;
            tmp = next;
        }
        root = NULL;
    }
```
Modificar el método dequeue() de MyQueue para devolver -1 si la cola está vacía
```C++
        int Dequeue(){
            if(!isEmpty()){
                int tmp = root->get_value();
                root=root->get_next();
                return tmp;
            }
            else
                cout<<"-1";
        }
```
Agregar el método peek() a la clase MyQueue para obtener el valor del primer elemento sin eliminarlo.
```C++
    int peek(){
        if(!isEmpty()){
            return root->get_value();
        }
        return -1;
    }
```
Agregar el método size() a la clase MyStack para obtener el número de elementos en la pila.
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
Agregar el método printInverted() de MyStack para imprimir los elementos en orden inverso.
```C++


```
Agregar el método clear() a la clase MyStack para eliminar todos los elementos de la pila.
```C++
void clear(){
    while(!this->isEmpty()){
        pop();
    }
}
```
Modificar el método pop() de MyStack para devolver -1 si la pila está vacía
```C++
        int pop(){
            if(!isEmpty()){
                int tmp = root->getValue();
                root=root->getNext();
                return tmp;
            }
            else
                return -1;
        }
```
Agregar el método peek() a la clase MyStack para obtener el valor del elemento superior sin eliminarlo.
```C++
int peek(){
    if(!isEmpty()){
        int top = pop();
        push(top);
        cout<<top;
    }
}
```
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
