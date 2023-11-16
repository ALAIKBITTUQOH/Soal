# Soal
1. Persamaan Non Linier
3+x^3-x=4

2. Persamaan Linier
2x-4=8

Intruksi :
1. Carilah Solusi dari 2 soal diatas (metode bebas)
2. Buatlah Program untuk mencari solusi diatas
3. tunjukkan nilai x di setiap iterasinya

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

# JAWABAN :
Untuk mencari solusi dari persamaan non-linier dan linier, kita dapat menggunakan metode iteratif seperti metode Newton-Raphson atau metode iterasi sederhana.
Berikut adalah contoh program Python menggunakan metode iterasi sederhana:

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Metode Iterasi Sederhana
def iterasi_sederhana(fungsi, x_awal, toleransi, maks_iterasi):
    x = x_awal
    iterasi = 0

    while iterasi < maks_iterasi:
        x_baru = fungsi(x)
        print(f"Iterasi {iterasi + 1}: x = {x_baru}")

        if abs(x_baru - x) < toleransi:
            return x_baru
        
        x = x_baru
        iterasi += 1

    print("Iterasi maksimum tercapai. Tidak ada solusi yang konvergen.")
    return None

# Persamaan Non Linier: 3 + x^3 - x = 4
def fungsi_non_linier(x):
    return x**3 - x + 1

# Persamaan Linier: 2x - 4 = 8
def fungsi_linier(x):
    return (x + 4) / 2

# Tentukan nilai awal, toleransi, dan maksimum iterasi
x_awal_non_linier = 1.0
x_awal_linier = 0.0
toleransi = 1e-6
maks_iterasi = 100

# Cari solusi untuk persamaan non-linier
solusi_non_linier = iterasi_sederhana(fungsi_non_linier, x_awal_non_linier, toleransi, maks_iterasi)

if solusi_non_linier is not None:
    print(f"Solusi persamaan non-linier: x = {solusi_non_linier}")

# Cari solusi untuk persamaan linier
solusi_linier = iterasi_sederhana(fungsi_linier, x_awal_linier, toleransi, maks_iterasi)

if solusi_linier is not None:
    print(f"Solusi persamaan linier: x = {solusi_linier}")

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

hasil output :
Iterasi 1: x = 1.0
Solusi persamaan non-linier: x = 1.0
Iterasi 1: x = 2.0
Iterasi 2: x = 3.0
Iterasi 3: x = 3.5
Iterasi 4: x = 3.75
Iterasi 5: x = 3.875
Iterasi 6: x = 3.9375
Iterasi 7: x = 3.96875
Iterasi 8: x = 3.984375
Iterasi 9: x = 3.9921875
Iterasi 10: x = 3.99609375
Iterasi 11: x = 3.998046875
Iterasi 12: x = 3.9990234375
Iterasi 13: x = 3.99951171875
Iterasi 14: x = 3.999755859375
Iterasi 15: x = 3.9998779296875
Iterasi 16: x = 3.99993896484375
Iterasi 17: x = 3.999969482421875
Iterasi 18: x = 3.9999847412109375
Iterasi 19: x = 3.9999923706054688
Iterasi 20: x = 3.9999961853027344
Iterasi 21: x = 3.999998092651367
Iterasi 22: x = 3.9999990463256836
Solusi persamaan linier: x = 3.9999990463256836
