
# **Actividad 1**: Cálculo de Hash

### **Objetivo:**
- Identificar la huella digital única de cada documento.

### **Instrucciones:**
- Para cada archivo PDF:
    + Lea el archivo.
    + Calcule el hash SHA-256.
    +  Complete las columnas 1 y 2 de la [Tabla 1](https://github.com/gpatigno/DISCRETAS_2026/blob/main/ACTIVIDAD3/Tabla.md) compartida.

******

#### Ejemplo en Python:

```python
import hashlib

with open("archivo.pdf", "rb") as f:
    data = f.read()

hash_val = hashlib.sha256(data).hexdigest()
print(hash_val)
```


*****