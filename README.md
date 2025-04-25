# ENTREGA 2

David Ruiz Vallejo
Yilmar David Jordan Murillo


-pred ≡ \n f x. n (\g h. h (g f)) (\u. x) (\u. u)

Explicación:

Esta es una forma clásica de definir el predecesor de un número en la codificación de Church.

La función aplica una técnica llamada "pair encoding", en la que se usa una estructura de par para rastrear el valor actual y el anterior durante la iteración.

n es el número Church del que queremos obtener el predecesor.

El resultado es otro número Church que representa n - 1.


-succ ≡ \n f x. f (n f x)
Explicación:

Esta es la definición estándar de sucesor en Church encoding.

Toma un número n, una función f y un valor inicial x.

Aplica f una vez más que n f x, es decir, hace n + 1 aplicaciones de f.


-iszero ≡ \m. m (\x t f. f) true
Explicación:

Esta función verifica si un número Church es igual a cero.

Aplica al número una función que siempre devuelve false y arranca con true.

Si el número aplica esa función cero veces, entonces se queda con true (es cero).

Si aplica al menos una vez, cambia a false.

