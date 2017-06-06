@author: paul valle
"""
from tkinter import *
# Definimos la clase App 
class App:
# Definimos el metdo con la palabra def luego el nombre que le queremos dar al metodo
# en este caso _init_  el cual inicializa los atributos del objetos que creamos ( se ejecuta inmediatamente luego de crear un objeto)
# seguido de self el cual lo utilizamos para hacer referencia a los
# atributos contenidos en la clase    
 def __init__(self, master):
        frame = Frame(master) # Frame utiliza areas rectangulares de la pantalla donde master representa la ventana padre
        frame.pack() #Crea un marco
        self.button = Button(frame, text="SALIR", fg="red",command=frame.quit) # Le asignamos el valor (texto) al atributo button de la clase
        self.button.pack(side=LEFT) # le damos la ubicaion de la ventana
        self.slogan = Button(frame,text="ENTRAR",command=self.write_slogan)
        self.slogan.pack(side=LEFT) #Posiciona la ventana en el lado indicado 
        
 def write_slogan(self):
        print ("Estamos aprendiendo a usar Tkinter!")  # define un metodo que pasa como atributo 
root = Tk()  #Inicializamos Tkinter, creamos un widget de raiz Tk
app = App(root) #instanciamos la clase App
root.mainloop()
