

# Funciones para manejar la pila de departamentos

def agregar_departamento(pila):
    depto = input("Ingrese el nombre del departamento: ").strip()
    if depto:
        pila.append(depto)
        print("Departamento agregado con éxito.")
    else:
        print("No ingresó ningún texto.")

def remover_departamento(pila):
    if len(pila) == 0:
        print("La pila está vacía, no se puede remover nada.")
    else:
        eliminado = pila.pop()
        print(f"Se removió el departamento: {eliminado}")

def imprimir_pila(pila):
    if len(pila) == 0:
        print("La pila está vacía.")
    else:
        print("\n--- Lista de Departamentos en la Pila ---")
        for depto in reversed(pila):
            print(depto)

def menu():
    pila_deptos = []
    
    while True:
        print("\n**** Menú de Opciones *****")
        print("1. Agregar departamento")
        print("2. Remover departamento")
        print("3. Imprimir pila")
        print("4. Salir")
        
        opcion = input("Seleccione una opción (1-4): ")
        
        if opcion == "1":
            agregar_departamento(pila_deptos)
        elif opcion == "2":
            remover_departamento(pila_deptos)
        elif opcion == "3":
            imprimir_pila(pila_deptos)
        elif opcion == "4":
            print("Saliendo del programa...")
            break
        else:
            print("Opción no válida. Intente de nuevo.")

# Ejecutar el programa
menu()

