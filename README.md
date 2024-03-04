import tkinter as tk
from tkinter import messagebox

class MyApplication:
    def __init__(self, root):
        self.root = root
        self.root.title("Complex GUI Application")
        self.root.geometry("400x300")

        # Create a label widget
        self.label = tk.Label(root, text="Welcome to Complex GUI Application", font=("Helvetica", 16))
        self.label.pack(pady=10)

        # Create a button widget
        self.button = tk.Button(root, text="Click Me", command=self.display_message)
        self.button.pack(pady=5)

        # Create an entry widget
        self.entry = tk.Entry(root)
        self.entry.pack(pady=5)

    def display_message(self):
        messagebox.showinfo("Message", f"You entered: {self.entry.get()}")

if __name__ == "__main__":
    root = tk.Tk()
    app = MyApplication(root)
    root.mainloop()
