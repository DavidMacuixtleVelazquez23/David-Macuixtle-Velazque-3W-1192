
print("David Macuixtle Velazquez")
# Crear un diccionario vacío
persona = {}

# Función para agregar información al diccionario
def agregar_dato():
    # Pedir al usuario el tipo de dato que quiere agregar (nombre, edad, etc.)
    tipo_dato = input("¿Qué dato quieres agregar (nombre, edad, sexo, teléfono, correo)? ").lower()
    valor_dato = input(f"Introduce el {tipo_dato}: ")
    
    # Agregar el dato al diccionario
    persona[tipo_dato] = valor_dato
    
    # Imprimir el contenido del diccionario
    print("Datos actuales de la persona:", persona)

# Ciclo para seguir pidiendo datos
while True:
    agregar_dato()
    # Preguntar si el usuario quiere seguir agregando datos
    continuar = input("¿Quieres agregar otro dato? (sí/no): ").lower()
    if continuar != "si":
        break

![image](https://github.com/user-attachments/assets/b6c5fd3f-f407-4beb-8259-c677bc72263f)
