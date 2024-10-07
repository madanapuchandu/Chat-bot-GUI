# ChatBot_GUI


```python
from tkinter import *
```
- This imports all the functions and classes from the `tkinter` module, which is a Python library used to create graphical user interfaces (GUIs).

```python
window = Tk()
```
- This creates the main application window (root window) for the GUI.

```python
window.title("UNQ CHAT BOT")
```
- This sets the title of the window to "UNQ CHAT BOT", which appears at the top of the window.

```python
window.geometry('400x500')
```
- This defines the size of the window to be 400 pixels wide and 500 pixels high.

```python
def send():
    send = "you:" + messagewindow.get()
```
- Defines a function `send()` that will be executed when the "Send" button is clicked. It retrieves the user's input from the `messagewindow` (text input area) and stores it in the `send` variable, prefixing it with "you:".

```python
    chatarea.insert(END, "\n" + send)
```
- This inserts the user's message (stored in `send`) into the `chatarea` (the area where chat messages are displayed), appending it to the end of the current text.

```python
    if messagewindow.get() == "hi":
        chatarea.insert(END, "\n" + "BOT: hello")
```
- If the user typed "hi", the bot responds with "hello" by inserting "BOT: hello" into the `chatarea`.

```python
    elif messagewindow.get() == "what is your name":
        chatarea.insert(END, "\n" + "BOT: my name is Chandu")
```
- If the user typed "what is your name", the bot responds with "my name is Chandu".

```python
    elif messagewindow.get() == "how are you":
        chatarea.insert(END, "\n" + "BOT: I am fine. what about you")
```
- If the user typed "how are you", the bot responds with "I am fine. what about you".

```python
    elif messagewindow.get() == "i am fine":
        chatarea.insert(END, "\n" + "BOT: good to hear that")
```
- If the user typed "i am fine", the bot responds with "good to hear that".

```python
    else:
        chatarea.insert(END, "\n" + "BOT: I didn't get that")
```
- If the user's input doesn't match any predefined phrases, the bot responds with "I didn't get that".

```python
chatarea = Text(window, bg='white', width=50, height=8)
chatarea.place(x=6, y=6, height=385, width=370)
```
- Creates a text widget `chatarea` where the chat conversation will be displayed.
  - `bg='white'` sets the background color to white.
  - `width=50` and `height=8` set the dimensions of the text area.
  - `place(x=6, y=6, height=385, width=370)` positions the `chatarea` at coordinates (6, 6) with a height of 385 and a width of 370 pixels.

```python
messagewindow = Entry(window, bg='white', width=30)
messagewindow.place(x=128, y=400, height=88, width=260)
```
- Creates an entry widget `messagewindow` where the user types their message.
  - `bg='white'` sets the background color of the entry widget.
  - `place(x=128, y=400, height=88, width=260)` positions the entry widget at coordinates (128, 400) with a height of 88 and a width of 260 pixels.

```python
send = Button(window, text="send", bg='blue', activebackground='light blue', width=20, height=5, font=('Arial', 12), command=send)
send.place(x=6, y=400, height=81, width=120)
```
- Creates a button labeled "send" that will call the `send()` function when clicked.
  - `bg='blue'` sets the background color of the button.
  - `activebackground='light blue'` sets the background color when the button is clicked.
  - `width=20` and `height=5` set the dimensions of the button.
  - `font=('Arial', 12)` sets the font to Arial with a size of 12.
  - `command=send` sets the function to be executed when the button is clicked.
  - `place(x=6, y=400, height=81, width=120)` positions the button at coordinates (6, 400) with a height of 81 and width of 120 pixels.

```python
window.mainloop()
```
- This starts the Tkinter event loop, which keeps the window open and responsive to user inputs (like clicking the "Send" button).