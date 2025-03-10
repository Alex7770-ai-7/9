import tkinter as tk

def convert():
    try:
        uah = float(entry.get())
        usd = uah / 41.2127  # Курс на 10.03.2025
        result.config(text=f"{uah:.2f} грн = {usd:.2f} $")
    except ValueError:
        result.config(text="Некорректное значение!")

root = tk.Tk()
root.title("Конвертер валют")

entry = tk.Entry(root)
entry.pack()

tk.Button(root, text="Конвертировать", command=convert).pack()
result = tk.Label(root, text="")
result.pack()

root.mainloop()
