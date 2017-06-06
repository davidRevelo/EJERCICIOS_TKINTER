# -*- coding: utf-8 -*-
"""
Created on Sat Jun 3 20:28:38 2017

@author: Byron
"""

from tkinter import*
root = Tk()
v = IntVar() # Declara variable de tipo entera
v.set(1)

#definimos las tuplas en la cual contiene un lenguaje de 
#programacion y un numero que es para la posicion
languages = [
        ("Python",1),
        ("Perl",2),
        ("Java",3),
        ("C++",4),
        ("C",5),
        ]

def ShowChoice():
    print (v.get()) 
# justify solo     
Label(root,
      text = """Choose your favourite programming language:""",
      justify = LEFT,
      padx = 20).pack()

#se usa for para mostrar todos lo lenguajes con su opcion para 
#seleccionar

for txt, val in languages:
    Radiobutton(root,
                text = txt,
                padx = 30,#Se usa para añadir espacio horizontal
                variable = v,
                command = ShowChoice(), #ejecuta esta funcion 
                value = val
                ).pack(anchor = W)
mainloop()#inicializa la ventana