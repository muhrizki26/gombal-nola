# gombal-nola
import tkinter as tk
from tkinter import messagebox
from PIL import Image, ImageTk
import random

# List gombalan
gombalan_list = [
    "Kamu tahu gak bedanya kamu sama bintang? Bintang ada di langit, kamu di hatiku.",
    "Kalau kamu bunga, aku lebahnya... selalu datang karena sayang.",
    "Aku gak bisa matematika, tapi aku tahu 1+1 = kita.",
    "Kamu tuh kayak kopi, bikin deg-degan setiap ketemu.",
    "Kalau kamu planet, aku mau jadi orbitnya, biar terus muterin kamu.",
    "Cintaku ke kamu tuh kayak software original... gak bisa dibajak orang lain.",
    "Dosa apa aku kemarin malam? Sampai pagi ini dikasih lihat bidadari seindah kamu.",
    "Kamu tuh kayak charger, bikin hidup aku full power setiap hari.",
    "Kalau kamu senyum, listrik PLN aja kalah terang.",
    "Kamu tahu gak, aku udah vaksin, tapi gak bisa sembuh dari virus cintamu."
]

def tampilkan_gombalan():
    gombal = random.choice(gombalan_list)
    messagebox.showinfo("💘 Gombalan maut buat wanita tercantik Nolaa 💘", gombal)

# Setup GUI
root = tk.Tk()
root.title("GOMBALAN UNTUK Cantikku")
root.geometry("400x500")
root.configure(bg="pink")

# Load dan tampilkan gambar
try:
    img = Image.open("pacarku.png")
    img = img.resize((200, 300), Image.LANCZOS)
    foto = ImageTk.PhotoImage(img)
    label_foto = tk.Label(root, image=foto, bg="pink")
    label_foto.pack(pady=10)
except:
    tk.Label(root, text="(Gambar tidak ditemukan)", bg="pink", fg="red").pack()

# Teks dan tombol
tk.Label(root, text="Khusus buat Nolaaa 😍", font=("Comic Sans MS", 16), bg="pink").pack(pady=10)
tk.Button(root, text="💌 Klik terus yaa cantik", font=("Arial", 12), command=tampilkan_gombalan, bg="white", fg="red").pack(pady=10)
tk.Label(root, text="~ dari Ikuuu yang selalu mikirin kamu ~", font=("Courier New", 10), bg="pink", fg="gray").pack(side="bottom", pady=20)

root.mainloop()
