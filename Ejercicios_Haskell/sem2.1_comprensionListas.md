1)Escribir un programa que calcule la suma de números naturales menores a 7. Usar comprensión de listas (x/x)
```Haskell
sum7 xs = sum [x|x<-xs, x<7]

main = do
    let lista = [1..10]
    putStrLn("La suma de los x < 7 es:" ++ show (sum7 lista))

ghci>[]
```

2)Escribir un programa que calcule la suma de números naturales pares menores de 7. Usar comprensión de listas (x/x)
```Haskell
sumapar7 xs = sum [x|x<-xs, even x, x<7]

main = do
    let lista = [1..10]
    putStrLn("La suma de los x pares < 7 es:" ++ show (sumapar7 lista))
```
3)Escribir un programa que calcule el producto de números naturales, menores a 7. Usar comprensión de listas (x/x)
```Haskell
producto7 xs = product [x|x<-xs, x<7]

main = do
    let lista = [1..10]
    print(producto7 lista)
```
4)Escribir un programa que calcule el producto de números naturales múltiplos de 3, menores a 7. Usar comprensión de listas (x/x)
```Haskell
prod xs = product [x|x<-xs,mod x 3 == 0, x<7]

main = do
    let lista = [1..10]
    print(prod lista)
```
5)Escribir un programa que muestre "aprobado" para un número mayor o igual que 11 y "desaprobado" en caso contrario para una lista inicial. Usar comprensión de listas (x/x) y lista inicial [19, 0, 11, 10, 20, 5]
```Haskell
calificar xs = [if x >= 11 then "Aprobado" else "Desaprobado"|x<-xs]

main = do
    let alumnos = [19,00,11,10,20,5]
    print(calificar alumnos)
```
6)Escribir un programa que sume dos listas (cada elemento de la lista1 con cada elemento de la lista2). La lista1 es [1, 2, 3], la lista2 es [4, 5, 6]. Usar comprensión de listas.
```Haskell
sumarlistas = zipWith(+)
main = do
    let lista1 = [1,2,3]
    let lista2 = [4,5,6]
    print(sumarlistas lista1 lista2)
```
7)Escribir un programa que usando la función filtroX devuelva una nueva lista con los elementos que pertenezcan a la listaX [1, 2, 3, 5, 8, 13]. Usar comprensión de listas. La listaA a filtrar es [1..10]
```Haskell
main = do
    let listaX = [1,2,3,5,8,13]
    let filtroX = [x | x <- [1..10], elem x listaX]
    putStrLn("el filtro de la listaX es:" ++ show filtroX)
```
8)Escribir un programa que usando la función sumprolen devuelva una nueva lista donde el primer elemento sea la suma de listaA, el segundo el producto de la listaA, y el tercero la longitud de la listaA. listaA [1, 2, 3, 4, 5]
```Haskell
main = do
    let a = [1,2,3,4,5]
    let suma = sum a
    let producto = product a
    let long = length a
    let lista = [suma,producto,long]
    print lista
```
9)Escribir un programa que usando la función distancia calcule la distancia euclidiana de un segmento. Un segmento es una matriz conformada por dos listas origen y destino, y cada lista tiene dos elementos "x" y "y". Calcule la distancia para la matrizA [[1, 1], [2, 2]]
```Haskell
main = do
    let matrizA = [[1,1],[2,2]]
    let lista0 = matrizA!!0
    let lista1 = matrizA!!1
    let x0 = lista0!!0
    let x1 = lista1!!1
    let y0 = lista0!!0
    let y1 = lista1!!1
    let dist = sqrt((x1-x0)^2 + (y1-y0)^2)
    print dist
```
10)Escribir un programa que calcule la distancia total entre 3 segmentos. Un segmento es una matriz conformada por dos listas origen y destino, y cada lista tiene dos elementos "x" y "y". La distancia total es la suma de las distancias de cada segmento. Use la función distancia para calcular la distancia para un segmento dado. Usar comprensión de lista. Calcule la distancia para la matrizX [[[1, 1], [2, 2]], [[2, 2], [3, 3]], [[3, 3], [4, 4]]]
