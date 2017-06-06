# EJERCICIOS_TKINTER

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
