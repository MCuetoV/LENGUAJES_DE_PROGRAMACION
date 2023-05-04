
11)Escriba un programa que reciba un número entero y una lista. 
Si el numero entero es par, devolver una nueva lista que contenga la lista inicial y el numero entero ingresado. Si no, devolver la lista inicial.
```Haskell
parList n lista = if even n then lista ++ [n] else lista

main = do
    let n = 9
        list = [1,2,3,4,5,6]
    putStrLn("la lista es: "++ show (parList n list))
```
12)Escriba un programa que reciba como entrada una lista de numeros enteros y devuelva su promedio entero.
```Haskell
promLista xs = sum xs/sum [1|_<-xs]

main = do
    let lista = [1..10]
    print (promLista lista)
```
13)Escribir un programa que reciba como entrada una lista de numeros enteros y un numero entero,
y devuelva una nueva lista donde cada uno de los elementos de la lista sea multiplicado por el numero entero ingresado.
```Haskell
multiplicarlista n xs = [x*n|x<-xs]
```
14)Escriba un programa que reciba como entrada una lista de años y devuelva una nueva lista con aquellos que son bisiestos. 
Tomar en cuenta que un año bisiesto es un año que puede ser divisible entre 4 (sin residuo) excepto cada año que es divisible entre 100 (sin residuo), 
a no ser que el año sea divisible entre 400 (sin residuo).
```Haskell
bisiesto año = año `mod` 4 == 0 && ((año `mod` 100 /= 0)||(año `mod` 400 == 0))

main = do
    let año = 2000
    print(bisiesto año)
```

15)Escriba un programa que reciba como entrada 2 listas, y devuelva una nueva lista con los elementos de la primera lista que existan en la segunda.
```Haskell
encomun :: (Eq a) => [a] -> [a] -> [a]
encomun[] _ = []
encomun(x:xs) ys
    | x `elem` ys = x : encomun xs ys
    | otherwise = encomun xs ys

main = do
    let lista1 = [1,2,3]
    let lista2 = [2,3,4]
    print (encomun lista1 lista2)
```
16)Escriba un programa que reciba un numero entero y devuelva una lista con su tabla de multplicar del 1 al 12.
```Haskell
tablamulti n = [x*n|x<-[1..12]
main = do
    print(tablamulti 7)
```
17)Escriba un programa que reciba una lista de istas de números enteros (lista de 2 nieveles o dimensiones, 
tambien conocida como matriz) y que devuelva una nueva lista con los promedios enteros de cada lista que tengan, por lo menos, 3 elementos.

18)Escriba un programa que reciba lista de numeros enteros y devuelva el valor del 3er elemento (usando head y tail). 
Si la lista tiene menos de 3 elementos, devolver 9999.

19)Escribir un programa que reciba una lista de Strings y un String, y devuelva True si la lista contiene el String o False si no lo contiene.

20)Escribir un programa que reciba una lista de Strings y un String. Si la lista no contiene el String ingresado,
devolver una nueva lista que agregue el String ingresado a la lista inicial. Si la lista lo contiene, devolver la lista inicial.


21)Escriba un programa que elimine los elementos duplicados de la siguiente lista de números enteros [1, 1, 2, 3, 3, 4, 4, 5].
``` Haskell
import Data.List

main = do
  let listaOriginal = [1, 1, 2, 3, 3, 4, 4, 5]
  print (listaSinDuplicados listaOriginal)

listaSinDuplicados [] = []
listaSinDuplicados lista = [head lista] ++ listaSinDuplicados(delete (head lista) (tail lista
```

22)Escriba un programa que reciba como entrada un número entero, si dicho valor no se encuentra en la lista añadirlo, 
caso contrario eliminarlo de la lista. Finalmente imprimir la lista ordenada ascendentemente. Trabajar con la siguiente lista [1, 3, 7, 12, 15, 20]
```Haskell
main = do
  let lista = [1, 3, 7, 12, 15, 20]
  putStrLn "Ingrese un número entero: "
  numero <- getLine
  let numeroInt = read numero :: Int
  let listaActualizada = actualizarLista numeroInt lista
  let listaOrdenada = sort listaActualizada
  print listaOrdenada

actualizarLista numero lista
  | numero `elem` lista = delete numero lista
  | otherwise = numero : lista
```

23)Escribir una función para calcular la pendiente de una recta, la función debe recibir dos parametros, 
cada uno es una lista de dos elementos (números enteros) que representan el punto A y punto B de la recta.
```Haskell
main = do
    let pendiente = calcularPendiente [10,5] [20,18]
    print (show pendiente)
calcularPendiente [x1, y1] [x2, y2] = (y2 - y1) / (x2 - x1)
```

24)Escriba un programa que calcule y añada a la lista los proximos 3 números siguiendo la sucesión de Fibonacci. 
Trabajar con la siguiente lista [0, 1, 1, 2, 3, 5, 8]
```Haskell
main = do
    let lista = [0, 1, 1, 2, 3, 5, 8]
    print (fibonacci lista)

fibonacci lista = do 
    let listaAux = reverse lista
    if length listaAux < 10
    then fibonacci(lista ++ [(head listaAux) + (head(tail(listaAux)))]) 
    else lista
```
25)Escriba un programa que reciba como entrada 2 listas de números enteros, las combine y elimine los elementos duplicados.
```Haskell
main = do
    print (unirListas [1,2,2,3] [3,4,5])

unirListas l1 l2 = do
    eliminarDuplicados(l1 ++ l2)


eliminarDuplicados [] = []
eliminarDuplicados l3 = [head l3] ++ eliminarDuplicados(delete (head l3) (tail l3))
```
26)Escriba un programa que reciba como parametro una cadena, extraiga las palabras y coloque cada una en una lista.

27)Escriba un programa que reciba como parametro una cadena y devuelva una lista de las vocales que se encuentren en la entrada sin que se repitan.

28)Escriba un programa que reciba como parametro n (un numero entero del 1 al 5), y replique los elementos de la lista n veces. Trabajar con la lista [1, 2, 3, 4, 5]
```Haskell
generarDuplicados n [] = []
generarDuplicados n lista = replicate n (head lista) ++ generarDuplicados n (tail lista)

main = do
    print(generarDuplicados 3 [1,2,3,4,5])
```
29)Escribir un programa que recorra una la lista [1, 3, 4, 5, 8, 9, 10] y la separe en dos sublistas de números pares e impares.
```Haskell
main = do
  let myList = [1, 3, 4, 5, 8, 9, 10]
  print (partition (even) (myList))
```
30)Escribir un programa que reciba como parametros una lista de números enteros y un número entero (n), 
devolver la lista filtrada en la que cada elemento cumpla la siguiente condición: < n.
```Haskell
filtrarLista lista n = filter (< n) lista 
main = do 
    print(filtrarLista [1,3,4,7,8,12,10,9] 9)
```
