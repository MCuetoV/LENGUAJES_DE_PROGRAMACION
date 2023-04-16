
1)Obtener el siguiente resultado:
Hello, everybody!
Please look at my favorite odd numbers: [11,13,15,17,19]
Usar https://www.haskell.org/get-started/

```Haskell
main = do
  putStrLn "Hello, everybody!"
  putStrLn ("Please look at my favorite odd numbers: " ++ show (filter odd[10 .. 20]))
```


2)Obtener
[-10,-9,-8,-7,-6,-5,-4,-3,-2,-1,0,1,2,3,4,5,6,7,8,9,10]
```Haskell
main = do
  putStrLn (show ([-10..10]))
```

3)Corregir el siguiente código
main = do
    let doubleMe x = x + 1
    putStrLn (show doubleMe 7)
    
4)Escribir un programa que permite hallar el doble del número 7 gracias a la función doubleMe.
```Haskell
main = do
  let doubleMe x = x * 2
  putStrLn (show (doubleMe 7))
```

5)Escribir un programa que permite hallar el factorial del número 5 gracias a la función fac.
```Haskell
main = do
    let fac n = if n == 0 then 1 else n * fac (n-1)
    putStrLn (show (fac 5))
```

6)Escribir un programa que permita ingrear un número y elevarlo al cuadrado gracias a la función square.
```Haskell
main = do
    let square x = x^2
    putStrLn("Ingresar numero: ")
    n <- readLn
    putStrLn("su cuadrado es: " ++ show (square(n)))
```

7)Escribir un programa que pida ingresar el resultado de 3 + 3 y que si es 6, imprima "ok", caso contrario "error"
```Haskell
main = do
    putStrLn("3+3 = ?")
    x <- readLn
    if x == 6 then putStrLn "OK" 
    else putStrLn "ERROR"
```
8)Escribir un programa que pida ingresar 2 números y devuelva la suma de los dos gracias a la función suma
```Haskell
main = do 
    putStrLn "Ingresar dos numeros a sumar."
    a <- readLn
    b <- readLn
    let suma x y = x + y
    putStrLn (show (suma a b))
```
9)Corregir el siguiente código especificando el tipo de dato correcto

main = do 
    m <- readLn
    putStrLn (show (m))
    
10)Escribir un programa que pida ingresar 2 números y devuelva el mayor de ellos. Sin usar función max.
```Haskell
main = do 
    putStrLn "Ingresar dos numeros a comparar: "
    putStrLn "A: "
    a <- readLn
    putStrLn "B: "
    b <- readLn
    let mayor x y = if x > y then x else y
    let m = mayor a b
    putStrLn ("El mayor es: " ++ show (m :: Int))))
```
11)scribir un programa que pida ingresar 3 números y devuelva el mayor de ellos. Usar función max
```Haskell
main = do
  putStrLn "Ingresar 3 numeros a comparar:"
  a <- readLn
  b <- readLn
  c <- readLn
  putStrLn ("El mayor es: " ++ show (max (a :: Int) (max (b :: Int) (c :: Int))))
```
12)Escribir un programa que pida ingresar un número y devuelva si es par o impar. Usar función even
```Haskell
main = do
    putStrLn"Ingresar numero:"
    n <- readLn
    putStrLn( "El numero ingresado es " ++ (if even n then "par." else "impar."))
```
13)Escribir un programa que pida ingresar un número y devuelva si es par o impar. Usar función odd
```Haskell
main = do
    putStrLn"Ingresar numero:"
    n <- readLn
    putStrLn( "El numero ingresado es " ++ (if odd n then "impar." else "par."))
```
14)Escribir un programa que pida ingresar un número y devuelva si es par o impar. Usar función mod
```Haskell
main = do
    putStrLn"Ingresar numero:"
    n <- readLn
    if mod n 2 == 0
        then putStrLn "El numero ingresado es par."
        else putStrLn "El numero ingresado es impar."
```
15)Escribir un programa que pida ingresar una cadena y devuelva su longitud.
```Haskell
main = do
    putStrLn"Ingresar cadena:"
    s <- getLine
    putStrLn(show(length s))
```
