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
