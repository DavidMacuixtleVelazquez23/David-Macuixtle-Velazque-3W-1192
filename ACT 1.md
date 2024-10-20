print("David Macuixtle Velazquez")
# Crear un diccionario de traducción
def crear_diccionario():
    # Pedimos al usuario que introduzca las palabras en el formato <palabra>:<traducción> separadas por comas
    entrada = input("Introduce las palabras y sus traducciones en el formato 'palabra:traducción' separadas por comas: ")
    pares = entrada.split(",")  # Separamos cada par por comas
    diccionario = {}  # Inicializamos un diccionario vacío
    
    for par in pares:
        palabra, traduccion = par.split(":")  # Separamos cada palabra y su traducción por dos puntos
        diccionario[palabra.strip()] = traduccion.strip()  # Añadimos la palabra y su traducción al diccionario
    
    return diccionario

# Función para traducir una frase palabra por palabra
def traducir_frase(diccionario):
    frase = input("Introduce una frase en español para traducir: ")
    palabras = frase.split()  # Dividimos la frase en palabras
    frase_traducida = []
    
    for palabra in palabras:
        # Si la palabra está en el diccionario, la traducimos; si no, la dejamos igual
        if palabra in diccionario:
            frase_traducida.append(diccionario[palabra])
        else:
            frase_traducida.append(palabra)
    
    # Unimos las palabras traducidas en una sola frase
    return " ".join(frase_traducida)

# Ejecución del programa
diccionario = crear_diccionario()
traduccion = traducir_frase(diccionario)
print("Frase traducida:", traduccion)

![image](https://github.com/user-attachments/assets/a1e8562b-8a59-4dc4-9efe-86474bace188)

