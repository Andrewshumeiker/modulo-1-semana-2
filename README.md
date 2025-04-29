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
