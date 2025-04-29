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

```python
#Ejericio 1 - 🧩 Gestión de Biblioteca

#Contexto:
#Una pequeña biblioteca necesita registrar sus libros en un sistema muy simple.
#Tareas:
#Crear: Agrega nuevos libros al diccionario. Cada libro tendrá: ID, Título, Autor, Año de publicación.
#Leer: Muestra todos los libros almacenados. Permite buscar un libro por su ID o Título.
#Actualizar: Modifica la información de un libro dado su ID. Ejemplo: cambiar el autor o el año de publicación.
#Eliminar: Elimina un libro de la biblioteca usando su ID.
biblioteca = {
    "001": {"título": "La vorágine", "autor": "José Eustasio Rivera", "año": 1924},
    "002": {"título": "Las intermitencias de la muerte", "autor": "José Saramago", "año": 2005},
    "003": {"título": "El club Dumas", "autor": "Arturo Pérez-Reverte", "año": 1993},
    "004": {"título": "Cien años de soledad", "autor": "Gabrel García Márquez", "año": 1967},
    "005": {"título": "La fiesta del chivo", "autor": "Mario Vargas Llosa", "año": 2000}
}
#Menu de opciones
menu = {
    "opción1": "agregar libro", "opción2": "buscar libro", "opción3": "actualizar", "opción4": "eliminar"
}
#Confirmación para acceder al menú
acceder_menu = input("¿Desea acceder al menú?: ")
if acceder_menu.lower() == "si":
    print(f"Estas son las opciones: \n{menu}")
    accion_usuario = input("Ingrese por favor, la acción que desea llevar a cabo ")
#Condicional que activa las acciones en caso de seleccionar la acción 1
    if accion_usuario == "1" or accion_usuario.lower() == "opcion 1":
        id_nuevo = input("Ingrese el nuevo ID del nuevo libro: ")
        titulo_nuevo = input("Ingrese el titulo ")
        autor_nuevo = input("Ingrese el autor: ")
        año_nuevo = input("Ingrese el año de publicación: ")
#se usa el método "setdefault" para crear una nueva "key" y posteriormente agregar la primer pareja "key" y "value"
        biblioteca.setdefault(id_nuevo,{}).setdefault("título", titulo_nuevo)
#se agrega el resto de la información del nuevo libro
        biblioteca[id_nuevo]["autor"] = autor_nuevo
        biblioteca[id_nuevo]["año"] = año_nuevo
        print(f"Se muestra la biblioteca actualizada: /n{biblioteca}")
#Opción 2 del menú
    elif accion_usuario == "2" or accion_usuario.lower() == "opcion 2":
        formato_busqueda = input("Ingrese \"1\" si desea buscar por ID. Ingrese \"2\" si desea buscar por título")
#Se ofrecen dos opciones de modo de búsqueda, dependiendo de cual elija, se da la información. 
        if formato_busqueda == "1":
            busqueda_usuario = input("Ingrese el ID del libro: ")
            titulo_buscado =  biblioteca[busqueda_usuario]["título"]
            print(f"El libro con el ID {busqueda_usuario}, corresponde al libro {titulo_buscado} y se encuentra disponible")
        elif formato_busqueda == "2":
           busqueda_usuario = input("Ingrese el título del libro: ")
#como no sabemos el ID del libro usamos for para que busque el titulo ingresado, a partir de una lista de los valores del diccionario
            lista_valores_diccionario = biblioteca.values()
            for valor in lista_valores_diccionario:
                 if valor == busqueda_usuario:
                     print(f"El libro {busqueda_usuario} se encuentra en el inventario")
                break
else:
    print("Gracias vuelva pronto")
```
