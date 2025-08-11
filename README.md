# Gestor-Tareas
Avance Diagrama de flujos 
Este proyecto es una aplicación en **Python** que permite administrar una lista de tareas desde la consola.  
Se desarrolló como parte de un ejercicio académico para aplicar conceptos de programación estructurada,  
uso de diagramas de flujo y manejo de control de versiones con Git y GitHub.

---
## Objetivos del Proyecto

- Implementar una aplicación funcional con **estructuras lógicas y repetitivas**.
- Utilizar **diagramas de flujo** para representar las funcionalidades principales.
- Configurar un repositorio en GitHub para la **gestión del código** y los **documentos del proyecto**.
- Aplicar **buenas prácticas de codificación**, incluyendo comentarios y control de errores.

---

## 📂 Estructura del Repositorio

gestor-tareas/
│
├── src/ # Código fuente de la aplicación
│ └── gestor_tareas.py
│
├── docs/ # Diagramas de flujo y documentación
│ ├── agregar_tarea.png
│ ├── listar_tareas.png
│ ├── eliminar_tarea.png
│ └── menu_principal.png
│
└── README.md # Documento principal del proyecto

## Funcionalidades

- **Agregar tarea**: Permite ingresar una nueva tarea a la lista.
- **Listar tareas**: Muestra todas las tareas registradas.
- **Eliminar tarea**: Elimina una tarea seleccionada por el usuario.
- **Menú interactivo**: Navegación sencilla mediante opciones numeradas.

- def agregar_tarea():
    tarea = input("Ingrese una nueva tarea: ")
    tareas.append(tarea)
    print("Tarea agregada correctamente.")

def listar_tareas():
    if not tareas:
        print("No hay tareas registradas.")
    else:
        for i, tarea in enumerate(tareas, 1):
            print(f"{i}. {tarea}")

def eliminar_tarea():
    listar_tareas()
    try:
        indice = int(input("Ingrese el número de la tarea a eliminar: "))
        if 0 < indice <= len(tareas):
            tareas.pop(indice - 1)
            print("Tarea eliminada correctamente.")
        else:
            print("Número de tarea inválido.")
    except ValueError:
        print("Entrada no válida.")

def menu():
    while True:
        print("\nGestor de Tareas")
        print("1. Agregar Tarea")
        print("2. Listar Tareas")
        print("3. Eliminar Tarea")
        print("4. Salir")
        opcion = input("Seleccione una opción: ")
        
        if opcion == "1":
            agregar_tarea()
        elif opcion == "2":
            listar_tareas()
        elif opcion == "3":
            eliminar_tarea()
        elif opcion == "4":
            break
        else:
            print("Opción inválida.")

if __name__ == "__main__":
    menu()

