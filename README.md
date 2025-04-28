# modulo-1-semana-2
#Determinar el estado de aprobación:
#Solicitar al usuario ingresar una calificación numérica (de 0 a 100)
#Evaluar si el estudiante ha aprobado o reprobado basándose en la calificación ingresada
```python
calificacion = int(input("ingrese la calificacion: "))
if calificacion <= 70:
    print("Reprobado !")
else:
 print ("aprobado")
```
```python
    suma = 0
for i in range (10):
    valor = float(input(f"ingrese el valor de {i+1}: "))
    suma += valor
promedio = suma / 10
print(f"el valor de la suma es {suma}")
print(f"el valor del promedio es {promedio}")
```
```python
suma = 0
for i in range(3):
    calificacion = float(input(f"ingrese la {i+1} calificacion: "))
    suma += calificacion
promedio = suma/3
print(f"el promedio es {promedio}")
print (f"las calificaciones son {calificacion}")
```
