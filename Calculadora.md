# -*- coding: utf-8 -*-
"""
Created on Sat Jun  3 21:10:55 2017

@author: Luis
"""

from tkinter import *

def clic(numeros):
    global operador
    operador = operador + str(numeros)
    tecla.set(operador)

def operaciones():
    global valor
    operacion=str(eval(valor))
    valores.set(operacion)
    valor=""

def borrar():
    global operador
    operador=""
    tecla.set("")

    
calculadora = Tk()
calculadora.title("Calculadora con funciones trigonométricas")

operador = ""
tecla = StringVar()

    
    
resultado = Entry(calculadora, font= ("arial", 15,"bold"), text = tecla,  bd =30, insertwidth = 4, justify = "right").grid(columnspan = 5)

btnc = Button(calculadora, padx= 15, bd =4,fg="black", font= ("arial", 15,"bold"), text = "sen").grid(row = 1, column=0)
btns = Button(calculadora, padx= 15, bd =4,fg="black", font= ("arial", 15,"bold"), text = "cos").grid(row = 1, column=1)
btnt = Button(calculadora, padx= 15, bd =4,fg="black", font= ("arial", 15,"bold"), text = "tan").grid(row = 1, column=2)
btnc = Button(calculadora, padx= 10, bd =4,fg="black", font= ("arial", 15,"bold"), text = "C", command = borrar).grid(row = 1, column=3)

btn7 = Button(calculadora, padx= 10, bd =4,fg="black", font= ("arial", 15,"bold"), text = "7", command = lambda:clic(7)).grid(row = 2, column=0) # lambda funcion anonima
btn8 = Button(calculadora, padx= 10, bd =4,fg="black", font= ("arial", 15,"bold"), text = "8", command = lambda:clic(8)).grid(row = 2, column=1)
btn9 = Button(calculadora, padx= 10, bd =4,fg="black", font= ("arial", 15,"bold"), text = "9", command = lambda:clic(9)).grid(row = 2, column=2)
btnd = Button(calculadora, padx= 10, bd =4,fg="black", font= ("arial", 15,"bold"), text = "/", command=lambda:clic("/")).grid(row = 2, column=3)

btn6 = Button(calculadora, padx= 10, bd =4,fg="black", font= ("arial", 15,"bold"), text = "6", command = lambda:clic(6)).grid(row = 3, column=0)
btn5 = Button(calculadora, padx= 10, bd =4,fg="black", font= ("arial", 15,"bold"), text = "5", command = lambda:clic(5)).grid(row = 3, column=1)
btn4 = Button(calculadora, padx= 10, bd =4,fg="black", font= ("arial", 15,"bold"), text = "4", command = lambda:clic(4)).grid(row = 3, column=2)
btnr = Button(calculadora, padx= 10, bd =4,fg="black", font= ("arial", 15,"bold"), text = "-",command=lambda:clic("-")).grid(row = 3, column=3)

btn3 = Button(calculadora, padx= 10, bd =4,fg="black", font= ("arial", 15,"bold"), text = "3", command = lambda:clic(3)).grid(row = 4, column=0)
btn2 = Button(calculadora, padx= 10, bd =4,fg="black", font= ("arial", 15,"bold"), text = "2", command = lambda:clic(2)).grid(row = 4, column=1)
btn1 = Button(calculadora, padx= 10, bd =4,fg="black", font= ("arial", 15,"bold"), text = "1", command = lambda:clic(1)).grid(row = 4, column=2)
btns = Button(calculadora, padx= 10, bd =4,fg="black", font= ("arial", 15,"bold"), text = "+",command=lambda:clic("+")).grid(row = 4, column=3)

btnp = Button(calculadora, padx= 10, bd =4,fg="black", font= ("arial", 15,"bold"), text = ".",command=lambda:clic('.')).grid(row = 5, column=0)
btni = Button(calculadora, padx= 10, bd =4,fg="black", font= ("arial", 15,"bold"), text = "=",command = operaciones).grid(row = 5, column=1)
btn0 = Button(calculadora, padx= 10, bd =4,fg="black", font= ("arial", 15,"bold"), text = "0", command = lambda:clic(0)).grid(row = 5, column=2)
btnm = Button(calculadora, padx= 10, bd =4,fg="black", font= ("arial", 15,"bold"), text = "x",command=lambda:clic("*")).grid(row = 5, column=3)


calculadora.mainloop() 