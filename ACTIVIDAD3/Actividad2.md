
# **Actividad 2**: Verificación de firma

### **Objetivo:**
- Determinar qué documentos fueron firmados correctamente

### **Instrucciones:**
- Para cada documento con firma:

    1.	Convertir hash a entero.
    2.	Calcular:

        `m = hash_int % n`

    3.	Verificar firma:

        `m_verificado = pow(s, e, n)`

    4.	Comparar:

        `m_verificado == m`

****