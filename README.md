# ENTREGA 2

David Ruiz Vallejo
Yilmar David Jordan Murillo


-These represent boolean values.

-(true) returns the first argument, while (false) returns the second.

-This behavior allows them to be used as conditional logic operators (like if-else).

-(pair)(m)(n) constructs a tuple-like structure by returning a function that expects a selector z.

-(fst)(p) retrieves the first element from the pair using the true function.

-(snd)(p) retrieves the second element using the false function.

-(I) is the identity function and is used here to represent 0.

-(S) is the successor function.

-It encodes a number by pairing (false) with the previous number.

-Think of it as: S(n) = (false, n)

-(P) is the predecessor function.

-When you apply (false) to a number created with (S), you extract its second element—i.e., the previous number.

-Since a numeral is encoded as a pair, this gives us access to its predecessor.

-(Zero)(n) tests whether (n) is zero.

-Since (zero = I), applying (true) to it returns (true)

-For any (n ≠ 0) (created via S), the pair structure returns (false).

-to_int(n) is a helper function to convert a Barendregt numeral to a Python integer.

-It repeatedly applies the predecessor function until an exception occurs (likely due to reaching a form that no longer supports further decomposition).

-pretty_print(n) also converts a numeral to an integer recursively.

-It uses the Zero test to determine if n is zero.

-Otherwise, it calls itself on the predecessor and adds 1.

-Outputs the result of applying S to 0 (should give 1).

-Applies P to 1 (the successor of 0), which should return 0.

-Verifies if the numeral is zero.

BIBLIOGRAFIA:

Barendregt, H. P. (1984). The Lambda Calculus: Its Syntax and Semantics (2nd ed.). North-Holland.

Replit Inc. (2025). Replit: The collaborative browser-based IDE. https://replit.com/

Python Software Foundation. (2025). The Python Language Reference, Release 3.11.5. https://docs.python.org/3/

Universidad de los Andes. (2025). Apuntes y materiales de clase sobre cálculo lambda. Departamento de Ciencias de la Computación.


