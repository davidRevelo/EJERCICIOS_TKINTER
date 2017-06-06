@author: paul valle
"""
print("EJERCICIO NUMERO 1")

#Utilizamos las etiquetas para empezar a llenar una ventana vacia, son muy utiles
# en la construccion de interfaces y formularios

# Comenzamos importando el módulo Tkinter.
# Contiene todas las clases, funciones y otras cosas necesarias para trabajar con el kit de herramientas Tk

from tkinter import *

#Inicializamos Tkinter, creamos un widget de raiz Tk

root = Tk()
# Creamos una etiqueta y la almacenamos en la variable etiqueta1

etiqueta1=Label(root,  text="HOLA TKINTER!")

# Utilizamos pack para ubicar nuestra etiqueta en la ventana

etiqueta1.pack()   
# El programa permanecera en el bucle de eventos hasta que cerremos la ventana

root.mainloop()