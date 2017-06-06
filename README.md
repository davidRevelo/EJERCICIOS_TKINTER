# EJERCICIOS_TKINTER

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



print("EJERCICIO NUMERO 2")
"MENSAJE WIDGET"
"SE UTILIZA PARA MOSTRAR MENSAJES DE TEXTO CORTOS"
from Tkinter import*
master=Tk()
whatever_you_do ="Whatever do yo will be insignificant, but it is very important that you do it.\n(Mahatma Gandhi)"
msg=Message(master, text=whatever_you_do)
msg.config(bg='lightgreen',font=('times',24,'italic')) #bg: el color del fondo que deseamos agregar, 
# font: es el mensaje de fondo tipo de letra, tañamo 
msg.pack()
mainloop()


print("EJERCICIO NUMERO 3")

#Comenzamos importando el modulo Tkinter
from tkinter import *

# Definimos la clase App 
class App:
# Definimos el metodo con la palabra def luego el nombre que le queremos dar al metodo
# en este caso _init_  el cual inicializa los atributos del objetos que creamos ( se ejecuta inmediatamente luego de crear un objeto)
# seguido de self el cual lo utilizamos para hacer referencia a los
# atributos contenidos en la clase    

 def __init__(self, master):
        frame = Frame(master)   # Frame utiliza areas rectangulares de la pantalla donde master representa la ventana padre
        frame.pack()   #Crea un marco
        self.button = Button(frame, text="SALIR", fg="red",command=frame.quit)  # Le asignamos el valor (texto) al atributo button de la clase
        self.button.pack(side=LEFT)  # le damos la ubicaion de la ventana
        self.slogan = Button(frame,text="ENTRAR",command=self.write_slogan)
        self.slogan.pack(side=LEFT)  #Posiciona la ventana en el lado indicado 
        
 def write_slogan(self):
        print ("Estamos aprendiendo a usar Tkinter!")  # define un metodo que pasa como atributo 

root = Tk()  #Inicializamos Tkinter, creamos un widget de raiz Tk
app = App(root) #instanciamos la clase App
root.mainloop() # El programa permanecera en el bucle de eventos hasta que cerremos la ventana



print("EJERCICIO NUMERO 4")
from tkinter import * #llamamos a la libreria tkinter
root = Tk()
v = IntVar()
Label(root, text="""Choose a programming language:""",justify = LEFT,padx = 20).pack() #Creamos un labeñ dando una justificaciopn en el espacio de la pantalla
Radiobutton(root, text="Python",padx = 20, variable=v, value=1).pack(anchor=W) #Creamos los radiobutton igual justificando en un espacio en nuestra pantalla
Radiobutton(root, text="Perl",padx = 20, variable=v, value=2).pack(anchor=W)
mainloop()



print("EJERCICIO NUMERO 5")
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


print("EJERCICIO NUMERO 6")
from tkinter import *
root = Tk()
v = IntVar()
v.set(1)  # inicializa la seleccion de las opciones de os radiobutton
languages = [
        ("Python",1),
        ("Perl",2),
        ("Java",3),
        ("C++",4),
        ("C",5)
]
def ShowChoice():
    print (v.get())

Label(root,                                         #creamos un label y ajustamos en la pantalla
      text="""Escoja un lenguaje de programación:""",
      justify = LEFT,
      padx = 20).pack()
for txt, val in languages:    #Creacion de los botones como radiobutton ya que al presionar se quedara en ON
    Radiobutton(root,
                text=txt,
                indicatoron =0,
                width = 20,
                padx = 20,
                variable=v,
                command=ShowChoice,
                value=val).pack(anchor=W)
mainloop()


print("EJERCICIO NUMERO 7")
from tkinter import*

master = Tk()

var1 = IntVar() #Declara variable de tipo entera
#Checkbutton es para crear una caja de seleccion 
Checkbutton(master, text = "Hombre", variable = var1).grid(row = 0,
           sticky=W)
var2 = IntVar() #se crea otra variable para otro crear otra caja con otro valor
Checkbutton(master,text="Mujer",variable=var2).grid(row=1,
           sticky=W)
mainloop()
# inicializa la ventana


print("EJERCICIO NUMERO 9")
"NOS PERMITE INGRESAR DATOS POR TECLADO"
"OBTENER CADENAS DE TEXTO, POR PARTE DEL USUARIO"
from Tkinter import*

master=Tk()
Label(master,text="First Name").grid(row=0)
Label(master,text="Last Name").grid(row=1)

e1=Entry(master) #Entry: aceptar cadenas de texto de una sola linea de un usuario
e2=Entry(master)

e1.grid(row=0,column=1)  #la posicion que deseamos fila, columna
e2.grid(row=1,column=1)
mainloop()
