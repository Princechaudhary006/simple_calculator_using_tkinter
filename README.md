# Simple Calculator using Tkinter
## By Prince Chaudhary
#Code
![](https://www.instagram.com/p/B9hUUf1HJ5vUSwJCgrxRbJwkcAlZt6dytRoHZM0/?igshid=1ttgoroe7ycr1)
from tkinter import *
import math

def click(event):
    global scvalue
    text =event.widget.cget("text")
    if text=="=":
       if scvalue.get().isdigit():
           value = int(scvalue.get())
       else:
           value = eval(Entry1.get())

       scvalue.set(value)
       Entry1.update() 
    elif text=="C":
        scvalue.set("")
        Entry1.update()
    else:
        scvalue.set(scvalue.get()+text)
        Entry1.update()


root =Tk()
root.geometry("300x450")
root.minsize(300,500)
root.maxsize(300,500)
root.configure(bg="gray")
root.title("Calculator")
scvalue =StringVar()
scvalue.set("")
Entry1 =Entry(root,textvar =scvalue,width=40,font=('lucida',20,"bold"))
Entry1.pack(pady=10,padx=10)

f=Frame(root)
f.configure(bg="gray")
b=Button(f,text="7",padx=10,pady =10,font="licida,20,bold")
b.pack(side=LEFT,padx=5,pady=5)
b.bind("<Button-1>",click)
b=Button(f,text="8",padx=10,pady =10,font="licida,20,bold")
b.pack(side=LEFT,padx=5,pady=5)
b.bind("<Button-1>",click)
b=Button(f,text="9",padx=10,pady =10,font="licida,20,bold")
b.pack(side=LEFT,padx=5,pady=5)
b.bind("<Button-1>",click)
b=Button(f,text="/",padx=10,pady =10,font="licida,20,bold",fg="red")
b.pack(side=LEFT,padx=5,pady=5)
b.bind("<Button-1>",click)
f.pack()


f=Frame(root)
f.configure(bg="gray")
b=Button(f,text="4",padx=10,pady =10,font="licida,20,bold")
b.pack(side=LEFT,padx=5,pady=5)
b.bind("<Button-1>",click)
b=Button(f,text="5",padx=10,pady =10,font="licida,20,bold")
b.pack(side=LEFT,padx=5,pady=5)
b.bind("<Button-1>",click)
b=Button(f,text="6",padx=10,pady =10,font="licida,20,bold")
b.pack(side=LEFT,padx=5,pady=5)
b.bind("<Button-1>",click)
b=Button(f,text="*",padx=10,pady =10,font="licida,20,bold",fg="red")
b.pack(side=LEFT,padx=5,pady=5)
b.bind("<Button-1>",click)
f.pack()

f=Frame(root)
f.configure(bg="gray")
b=Button(f,text="1",padx=10,pady =10,font="licida,20,bold")
b.pack(side=LEFT,padx=5,pady=5)
b.bind("<Button-1>",click)
b=Button(f,text="2",padx=10,pady =10,font="licida,20,bold")
b.pack(side=LEFT,padx=5,pady=5)
b.bind("<Button-1>",click)
b=Button(f,text="3",padx=10,pady =10,font="licida,20,bold")
b.pack(side=LEFT,padx=5,pady=5)
b.bind("<Button-1>",click)
b=Button(f,text="-",padx=10,pady =10,font="licida,20,bold",fg="red")
b.pack(side=LEFT,padx=5,pady=5)
b.bind("<Button-1>",click)
f.pack()


f=Frame(root)
f.configure(bg="gray")
b=Button(f,text="=",padx=10,pady =10,font="licida,20,bold",fg="red")
b.pack(side=LEFT,padx=5,pady=5)
b.bind("<Button-1>",click)
b=Button(f,text="0",padx=10,pady =10,font="licida,20,bold")
b.pack(side=LEFT,padx=5,pady=5)
b.bind("<Button-1>",click)
b=Button(f,text="C",padx=10,pady =10,font="licida,20,bold",fg="red")
b.pack(side=LEFT,padx=5,pady=5)
b.bind("<Button-1>",click)
b=Button(f,text="+",padx=10,pady =10,font="licida,20,bold",fg="red")
b.pack(side=LEFT,padx=5,pady=5)
b.bind("<Button-1>",click)
f.pack()
Label1=Label(root,text ="Developed by Prince Chaudhary")
Label1.configure(bg="gray")
Label1.pack(side=BOTTOM,pady=20)
root.mainloop()
