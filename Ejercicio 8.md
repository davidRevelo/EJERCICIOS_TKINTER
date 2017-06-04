# -*- coding: utf-8 -*-
"""
Created on Sat Jun  3 19:29:24 2017

@author: Luis
"""

from tkinter import *
master = Tk()

def var_states():
    var1 = IntVar()   # Declara variable de tipo entera
    var2 = IntVar()   # Declara variable de tipo entera
    
            
    print (" male: ",var1.get())  # imprime un mensaje y muestra el valor de la variable var1 con el metodo get()
    print ("female: ",var2.get()) # imprime un mensaje y muestra el valor de la variable var2 con el metodo get()
    
    Label(master, text="Indicar el sexo:").grid(row=0, sticky=E) # Se implementa un cuadro de pantalla donde se puede colocar texto 
                                                                 # o imagenes,ademas de agregar una cuadricula  en la posición 0 y el texto
                                                                 # colocado en el sector oeste (W) 
    
    
    Checkbutton(master, text="male", variable= var1).grid(row=1,sticky=W) # Se crea un Checkbutton en la fila 1 en la región oeste de la pantalla
    
    Checkbutton(master, text="female", variable=var2).grid(row=2,sticky=W) # Se crea un Checkbutton en la fila 2 en la región oeste de la pantalla
    
    Button(master, text='Quit', command= master.quit).grid(row=3,sticky=W, padx=4) # Se crea un boton, al presionarlo la pantalla se cerrará
                                                                                    # Se coloca en la fila 3, padx = 4 es la distancia que tendra el 
                                                                                    # boton hacia la derecha.
                                                                                    
    Button(master, text='Show', command=var_states).grid(row=4,sticky=W, pady=4)   # Se crea un boton, al presionarlo la pantalla se restablecera
                                                                                    # Se coloca en la fila 3, pady = 4 es la distancia que tendra el 
                                                                                    # boton hacia la abajo.

var_states()  # Se llama al metodo var_states
mainloop()  # Se inicializa la ventana