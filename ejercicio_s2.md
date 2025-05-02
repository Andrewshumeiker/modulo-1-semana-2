#ejercicio practica cajero
```python
saldo = 50
while True:
    opcion = str(input("qué desea hacer? \n retirar \n depositar \n saldo \n salir \n"))
    if opcion == "retirar":
        retiro = float(input("ingrese el monto de retiro: "))
        if retiro <= saldo:
            saldo -= retiro
            print(f" saldo restante: {saldo}")
        else:
            print("saldo insuficiente!")
    elif opcion == "depositar":
        deposito = float(input("ingrese el monto de deposito: "))
        saldo += deposito 
        print (f"su saldo es {saldo}")
    elif opcion == "saldo":
        print(saldo)
    elif opcion == "salir":
        print("hasta pronto!")
        break
    else:
        print(f"seleccion inválida \n {opcion}")
```
