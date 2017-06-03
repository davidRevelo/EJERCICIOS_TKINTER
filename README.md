# EJERCICIOS_TKINTER

print("EJERCICIO NUMERO 2")
from Tkinter import*
master=Tk()
whatever_you_do ="Whatever do yo will be insignificant, but it is very important that you do it.\n(Mahatma Gandhi)"
msg=Message(master, text=whatever_you_do)
msg.config(bg='lightgreen',font=('times',24,'italic'))
msg.pack()
mainloop()

print("EJERCICIO NUMERO 9")
from Tkinter import*

master=Tk()
Label(master,text="First Name").grid(row=0)
Label(master,text="Last Name").grid(row=1)

e1=Entry(master)
e2=Entry(master)

e1.grid(row=0,column=1)
e2.grid(row=1,column=1)
mainloop()