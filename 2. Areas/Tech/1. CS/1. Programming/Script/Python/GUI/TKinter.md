1. Init Window
```python
from tkinter import *
window = Tk()
window.mainloop()
```

2. Label
```python
# Container name, text, background, foreground, font, padding(distance between object and border)
Label = Label(window,
			  text="Hello",
			  bg="black",
			  fg="white",
			  font=("Arial",40,"bold"),
			  padx=20,
			  pady=20)
# Pack Label in the window
Label.pack()
```

3. Button
```python
count = 0
def click():
	global count
	count+=1
	print(count)

Button = Button(window,
			   text="click me",
			   command=click,
			   bg = "black",
			   fg = "green",
			   activeforeground = "green",
			   activebackground = "black")

Button.pack()
```