# project
import os
import random
import string
data = dict()
while True:
    os.system("cls")   
    print(f"{'DATA KEUANGAN':^45}")  

    keyFinal = "".join(random.choice(string.ascii_uppercase) for _ in range(3))
    tanggal = input("Tanggal Transaksi\t\t: ")
    deskripsi = input("Deskripsi\t\t\t: ")
    harga = input("Harga\t\t\t\t: ")

    
    data[keyFinal] = {
        'tanggaltransaksi': tanggal,
        'deskripsi': deskripsi,
        'harga': harga
    }

    opsi = input("Input data lagi (y/t) : ").lower()
    if opsi == 't':
        break


print("-" * 60)
print(f"Key\t Tanggal Transaksi\t Deskripsi\t Harga")
print("-" * 60)

for key, value in data.items():
    print(f"{key}\t {value['tanggaltransaksi']}\t {value['deskripsi']}\t {value['harga']}")
