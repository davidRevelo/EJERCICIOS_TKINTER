# EJERCICIOS_TKINTER

print("EJERCICIO NUMERO 2")
from Tkinter import*
master=Tk()
whatever_you_do ="Whatever do yo will be insignificant, but it is very important that you do it.\n(Mahatma Gandhi)"
msg=Message(master, text=whatever_you_do)
msg.config(bg='lightgreen',font=('times',24,'italic'))
msg.pack()
mainloop()