
# **Ejercicio 4**: Generación de claves y firma digital

### **Objetivo:**
- Comprender el proceso completo de RSA: Generación de claves y firma digital.

### **Instrucciones:**
- **Parte A**: Generación de claves RSA.
    * Con sus compañeros de grupo, genere su propio par de claves pública y privada:
    1.	Elegir dos números primos pequeños menores a 1000:
        ```python
        p = 
        q = 
        ```

    2.	Calcular:
        ```python
        n = p * q
        phi = (p - 1) * (q - 1)
        
        print("n =", n)
        print("phi(n) =", phi)
        ```

    3.	Elegir un número e tal que gcd(e, φ(n)) = 1:
        ```python
        import math

        e = 17
        print("gcd(e, phi) =", math.gcd(e, phi))
        4.	Calcular d tal que d ≡ e⁻¹ mod φ(n):
        d = pow(e, -1, phi)
        print("d =", d)
        ```


- **Parte B**: Firma digital.
    * Firme el documento llamado [CartaEstudiante.pdf](https://github.com/gpatigno/DISCRETAS_2026/blob/main/ACTIVIDAD3/CartaEstudiante.pdf), siguiendo el siguiente procedimiento:

    1.	Leer el archivo pdf y calcule hash:

        ```python
        import hashlib

        with open("CartaEstudiante.pdf", "rb") as f:
            data = f.read()

        hash_hex = hashlib.sha256(data).hexdigest()
        hash_int = int(hash_hex, 16)

        print("Hash (hex):", hash_hex)
        ```    

    2.	Reduzca este Hash mediante la operación **módulo n**:
        ```python
        m = hash_int % n
        print("m =", m)
        ```

    3.	Firmar con clave privada:
        ```python
        s = pow(m, d, n)
        print("Firma s =", s)        
        ```

- **Parte C**: Verificación de su firma digital realizada.
    * Con este archivo firmado, realice nuevamente el [Ejercicio No. 1](https://github.com/gpatigno/DISCRETAS_2026/blob/main/ACTIVIDAD3/Ejercicio1.md) de esta actividad.
    * Se verifica que su firma digital es válida? **Explique**.
    * Complete la quinta fila de la [Tabla 1](https://github.com/gpatigno/DISCRETAS_2026/blob/main/ACTIVIDAD3/Tabla.md) con la información de su **CartaEstudiante** firmada digitalmente.

******
