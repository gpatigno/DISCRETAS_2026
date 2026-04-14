
# **Ejercicio 2**: Verificación de firma

### **Objetivo:**
- Determinar la autencidad de la firma de diferentes documentos.

### **Instrucciones:**
- Para cada documento con firma:

    1.	Convertir su Hash a entero.
    2.	Calcular:

        `m = hash_int % n`

    3.	Verificar la firma compartida:

        `m_verificado = pow(s, e, n)`

    4.	Comparar la firma compartida con la esperada según el Hash:

        `m_verificado == m`

    5. La firma compartida es entonces válida? **Explique**.
    6. Complete las columnas 3, 4 y 5 de la [Tabla 1](https://github.com/gpatigno/DISCRETAS_2026/blob/main/ACTIVIDAD3/Tabla.md).


### **Preguntas:**
- ¿Por qué falla la verificación?
- ¿Qué propiedad criptográfica se evidencia?


****