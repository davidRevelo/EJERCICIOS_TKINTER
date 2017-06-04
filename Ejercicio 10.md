# -*- coding: utf-8 -*-
"""
Created on Sat Jun  3 20:24:18 2017

@author: Luis
"""

from tkinter import *

def show_entry_fields():
    print("First Name: %s\nLast Name: %s" % (e1.get(), e2.get()))   # Se crea una función donde se mostrará lo escrito tanto en el 
                                                                    # grid e1 como en el e2 

master = Tk()
Label(master, text="First Name").grid(row=0) # Se crea un label en la fila 0
Label(master, text="Last Name").grid(row=1)  # Se crea un label en la fila 1

e1 = Entry(master) # Se crea una variable, entry que se utiliza para aceptar cadenas de texto de una sola línea de un usuario.
e2 = Entry(master)

e1.grid(row=0, column=1) # se crea un grid en la fila 0 y en la columna 1 
e2.grid(row=1, column=1) # se crea un grid en la fila 1 y en la columna 1

Button(master, text='Quit', command=master.quit).grid(row=3,column=0, sticky=W, pady=4) # Se crea un boton, al presionarlo la pantalla se cerrará
                                                                                        # Se coloca en la fila 3, pady = 4 es la distancia que tendra el 
                                                                                        # boton hacia abajo.
                                                                                        
Button(master, text='Show',command=show_entry_fields).grid(row=3, column=1, sticky=W,pady=4)# Se crea un boton, al presionarlo imprimirá lo que hayamos escrito
                                                                                            # en cada uno de los grids 
                                                                                            # Se coloca en la fila 3 y en la columna 0, pady = 4 es la distancia que tendra el 
                                                                                            # boton hacia la abajo.


show_entry_fields() # Se llama a la funcion show_entry_fields

mainloop( ) # Se inicializa la ventana