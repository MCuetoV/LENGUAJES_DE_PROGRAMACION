1)Escribir un programa que calcule la suma de los elementos de una lista de números enteros. La lista es [1, 2, 3, 4, 5]
```Haskell
main = do
    let lista = [1,2,3,4,5]
    putStrLn(show (sum lista))
    
--Usando ghci> se demostro como se pudo hacer pero con: lista!!0 + lista!!1 + lista!!2... 
    
```
2)Escribir un programa que calcule la suma de los elementos impares de una lista de números enteros
```Haskell
main = do
    let lista = [1,2,3,4,5]
    putStrLn(show (sum (filter odd lista)))
    
--ghci> sum(filter odd lista)
---18
```
3)Escribir un programa que calcule el producto de los elementos de una lista de números enteros. La lista es [1, 2, 3, 4, 5]
```Haskell
main = do
    let lista = [1,2,3,4,5]
    putStrLn(show(product(lista)))
    
--ghci> product(lista)
```
4)Escribir un programa que calcule el producto de los elementos pares de una lista de números enteros. La lista es [1, 2, 3, 4, 5]
```Haskell
main = do
    let lista = [1,2,3,4,5]
    putStrLn(show(product(filter even lista)))
    
--ghci> product(filter even lista)
```
5)Escribir un programa que concatene dos listas. La lista1 es [1, 2, 3], la lista2 es [4, 5, 6]
```Haskell
--ghci> [1,2,3] ++ [4,5,6]
```
6)Escribir un programa que invierta una lista. La lista es [1, 2, 3, 4, 5]
```Haskell
--ghci> reverse lista
```
7)Escribir un programa que calcule la suma de los elementos de una lista que sean mayores o iguales a 3. La lista es [1, 2, 3, 4, 5]
```Haskell
main = do
    let lista = [1,2,3,4,5]
    let mayortres elem = elem >= 3 
    putStrLn(show(sum(filter mayortres lista)))

--ghci> let mayortres elem = elem >= 3
--ghci> sum(filter mayortres lista)
 
```
8)Escribir un programa que calcule la cantidad de los elementos de una lista que sean menores que 3. La lista es [1, 2, 3, 4, 5]
```Haskell
main = do
    let lista = [1,2,3,4,5]
    let menortres elem = elem < 3
    putStrLn(show(length(filter menortres lista)))
 
 --ghci> menortres elem = elem < 3
 --ghci> length(filter menortres lista)
 
```
9)Escribir un programa que devuelva True si todos los elementos son mayores que 0, o False en caso contrario. La lista es [1, 2, 3, 4, 5]
```Haskell
main = do
    let lista = [1,2,3,4,5]
    let mayorcero elem = elem > 0
    putStrLn(show(lista == (filter mayorcero lista)))
```
10)Escribir un programa que devuelva True si algún elemento es igual a 10, o False en caso contrario. La lista es [10, 2, 3, 4, 5]
```Haskell
main = do
    let lista = [1,2,3,10,4,5] --probando con un elemento 10; preguntar como seria con varios 10s
    let igualdiez elem = elem == 10
    putStrLn(show((filter igualdiez lista) == [10]))
```
