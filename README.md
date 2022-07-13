from tkinter import *
from tkinter.ttk import * 
from time import strftime

dk = Tk()
dk.title('Clock')
dk.minsize(width=610, height=110)
dk.maxsize(width=650, height=120)
label = Label(dk, font=('ds-digital', 80), background="black", foreground="green")
label.pack(anchor='center')
def time():
	string = strftime('%H:%M:%S:%p')
	label.config(text=string)
	label.after(100, time)

time()
dk.mainloop()
