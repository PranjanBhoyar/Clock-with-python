# Clock-with-python
A digital clock showing time with the help of python code.



from tkinter import *
from tkinter.ttk import *

from time import strftime

root= Tk()
root.title("Aapli Ghadyal")

def time():
    string= strftime('%H:%M:%S %p')
    label.config(text=string)
    label.after(1000, time)

label= Label (root, font=("ds-digital", 80), background="black" , foreground="cyan")
label.pack(anchor='center')
time()

mainloop()
