# Random-password-generator-
import tkinter    #import required packages
from tkinter import *
import random

#tkinter
tk=tkinter.Tk()
tk.title('RANDOM-PASSWORD GENARATOR')
tk.geometry('700x700')

#delete function 
def clear():
    eent.delete(0,END)

def function():
    num='1234567890' 
    lettup='ABCDEFGHIJKLMNOPQRSTUVWXYZ'
    lettsm='abcdefghijklmnopqrstuvwxyz'
    symbol='@_'
    total=num+lettup+lettsm+symbol
    len=12
    pas=''.join(random.sample(total,len))
    eent.insert(0,pas)
      
               
    
    
    
    
    

eent=Entry(tk,width=20,relief=RIDGE, justify=CENTER)
eent.grid(row=0,column=0,padx=100,pady=50)


but=Button(tk,text='RANDOM',font=('arial',7),relief=RAISED,bd=5,command=function)
but.grid(row=1,column=0,padx=150,pady=50)


cl=Button(tk,text='CLEAR',font=('arial',7),relief=RAISED,bd=5,command=clear)
cl.grid(row=2,column=0,padx=150,pady=50)


tk.mainloop()
