# modulo-1-semana-2
#Determinar el estado de aprobación:
Solicitar al usuario ingresar una calificación numérica (de 0 a 100)
Evaluar si el estudiante ha aprobado o reprobado basándose en la calificación ingresada
```python
calificacion = int(input("ingrese la calificacion: "))
if calificacion <= 70:
    print("Reprobado !")
else:
 print ("aprobado")
```
Calcular el promedio:
Permitir al usuario ingresar una lista de calificaciones (separadas por comas)
Calcular y mostrar el promedio de las calificaciones en la lista
```python
calificaciones = (input(f"calificaciones que quiere promediar: "))
lista = [float(n) for n in calificaciones.split(",")]
promedio = sum(lista)/ len(lista)
print(f"promedio de calificaciones: {promedio:.2f}")
```
```python
entrada = (input("ingrese las calificaciones separadas por comas: "))
calificaciones = entrada.split(",")
suma = 0
cantidad = 0
for i in calificaciones:
    nota =float(i.strip())
    suma += nota
    cantidad += 1
promedio = suma/cantidad
print(f"el promedio es : {promedio}")
```
```python
print("ingrese calificaciones una por una y escriba -5 para finalizar: ")
contador = 0
entrada = float(input("ingrese las calificaciones: "))
while entrada != -5:
    if entrada > 70:
        contador += 1
    entrada = float(input("ingrese otra calificacion (-5 para finalizar): "))
print(f"la cantidad de numeros mayores a 70 son {contador}")

```
```python
entrada = (input("ingrese las calificaciones separadas por comas: "))
calificaciones = entrada.split(",")
buscada =float(input("qué calificacion deseas buscar: "))
cantidad = 0
for i in calificaciones:
    nota =float(i.strip())
    if nota != buscada:
        continue
    cantidad += 1
    if cantidad == 3:
     print(f"la calificacion {buscada} ya apareció más de 3 veces")
     break
print(f"la calificacion {buscada} apareció {cantidad} veces")
```




```python
# ----------------------------------------
# 1. DETERMINAR ESTADO DE APROBACIÓN
# ----------------------------------------

# Se solicita al usuario una calificación entre 0 y 100
calificacion = float(input("Ingrese la calificación (0-100): "))

# Validamos si la calificación está en el rango válido
if calificacion < 0 or calificacion > 100:
    print("Calificación no válida.")
# Si es menor a 70, se considera reprobado
elif calificacion < 70:
    print("Reprobado!")
# Si es mayor o igual a 70, está aprobado
else:
    print("Aprobado!")

# ----------------------------------------
# 2. CALCULAR PROMEDIO (sin usar split)
# ----------------------------------------

# El usuario ingresa una lista de calificaciones separadas por comas (ej: 70,80,90)
texto = input("Ingrese las calificaciones separadas por comas: ")

acumulador = ""    # Para ir formando cada número
suma = 0.0         # Suma total de las calificaciones
contador = 0       # Cantidad de calificaciones

# Recorremos el texto carácter por carácter
for caracter in texto:
    if caracter != ",":
        acumulador += caracter  # Acumulamos los dígitos del número
    else:
        # Cuando encontramos una coma, convertimos lo acumulado a número
        numero = float(acumulador)
        suma += numero
        contador += 1
        acumulador = ""  # Reiniciamos para el próximo número

# Agregamos el último número (que no termina en coma)
if acumulador != "":
    numero = float(acumulador)
    suma += numero
    contador += 1

# Calculamos y mostramos el promedio
promedio = suma / contador
print(f"Promedio de calificaciones: {promedio:.2f}")

# ----------------------------------------
# 3. CONTAR CALIFICACIONES MAYORES A 70 (usando while)
# ----------------------------------------

print("\nIngrese calificaciones una por una y escriba -5 para finalizar:")

contador_mayores = 0  # Contador de calificaciones mayores a 70

# Primera entrada del usuario
entrada = float(input("Ingrese la calificación: "))

# Mientras no se ingrese -5, seguimos leyendo calificaciones
while entrada != -5:
    if entrada > 70:
        contador_mayores += 1  # Sumamos si es mayor a 70
    entrada = float(input("Ingrese otra calificación (-5 para finalizar): "))

# Mostramos el total
print(f"La cantidad de calificaciones mayores a 70 es: {contador_mayores}")

# ----------------------------------------
# 4. VERIFICAR Y CONTAR UNA CALIFICACIÓN ESPECÍFICA (con break y continue)
# ----------------------------------------

# El usuario ingresa otra lista de calificaciones separadas por coma
texto2 = input("\nIngrese nuevamente calificaciones separadas por comas: ")

# Se solicita la calificación a buscar
buscada = float(input("¿Qué calificación deseas buscar?: "))

acumulador = ""  # Para ir formando los números
cantidad = 0     # Contador de veces que aparece la calificación buscada

# Recorremos carácter por carácter como antes
for caracter in texto2:
    if caracter != ",":
        acumulador += caracter
    else:
        numero = float(acumulador)
        acumulador = ""  # Reiniciar acumulador para el siguiente número

        # Si no es la que buscamos, pasamos a la siguiente (continue)
        if numero != buscada:
            continue

        cantidad += 1  # Contamos la coincidencia

        # Si aparece 3 veces, se detiene el ciclo (break)
        if cantidad == 3:
            print(f"La calificación {buscada} apareció 3 veces. Se detiene la búsqueda.")
            break

# Verificamos si quedó un último número por procesar
if acumulador != "":
    numero = float(acumulador)
    if numero == buscada:
        cantidad += 1

# Mostramos el total de veces que apareció
print(f"La calificación {buscada} apareció {cantidad} veces.")
```
