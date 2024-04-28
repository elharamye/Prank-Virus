import tkinter as tk

def on_closing():
    for _ in range(2):
        root_new = tk.Tk()
        root_new.title("Intel(R) Dynamic Application Loader Host Interface")
        root_new.protocol("WM_DELETE_WINDOW", on_closing) 
        root_new.bind("<Key>", check_key_press) 
        label = tk.Label(root_new, text="Ops...")
        label.pack()
        open_windows.append(root_new)

def check_key_press(event):
    if event.keysym == 'Shift_L' and event.state & 0x4: 
        for window in open_windows:
            window.destroy()
        open_windows.clear()

open_windows = []

root = tk.Tk()
root.title("Intel(R) Dynamic Application Loader Host Interface")  
root.protocol("WM_DELETE_WINDOW", on_closing) 
root.bind("<Key>", check_key_press) 
label = tk.Label(root, text="Ops...")
label.pack()

open_windows.append(root)

root.mainloop()

# TO CLOSE ALL JUST PRESS CTRL_L AND SHFIT_L
