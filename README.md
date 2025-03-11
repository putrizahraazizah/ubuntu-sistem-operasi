# ubuntu-sistem-operasi

**1. Membuat Program Kalkulator**
Kita akan membuat kalkulator sederhana yang dapat melakukan operasi penjumlahan, pengurangan, perkalian, dan pembagian.

def tampilkan_menu():
    print("======= KALKULATOR =======")
    print("1. Penjumlahan")
    print("2. Pengurangan")
    print("3. Perkalian")
    print("4. Pembagian")
    print("5. Keluar")
    print("==========================")

def operasi_matematika(angka1, angka2, pilihan):
    if pilihan == '1':
        return angka1 + angka2, " + "
    elif pilihan == '2':
        return angka1 - angka2, " - "
    elif pilihan == '3':
        return angka1 * angka2, " * "
    elif pilihan == '4':
        return (angka1 / angka2 if angka2 != 0 else "Error: Pembagian dengan nol tidak diperbolehkan!"), " / "
    else:
        return None, None

def jalankan_kalkulator():
    while True:
        tampilkan_menu()
        pilihan = input("Pilih operasi (1-5): ")
        
        if pilihan == '5':
            print("Terima kasih telah menggunakan kalkulator!")
            break

        if pilihan in ['1', '2', '3', '4']:
            try:
                angka1 = float(input("Masukkan angka pertama: "))
                angka2 = float(input("Masukkan angka kedua: "))
                hasil, simbol = operasi_matematika(angka1, angka2, pilihan)
                if hasil is not None:
                    print(f"Hasil: {angka1}{simbol}{angka2} = {hasil}")
            except ValueError:
                print("Error: Harap masukkan angka yang valid!")
        else:
            print("Error: Pilihan tidak tersedia, silakan pilih lagi!")

if _name_ == "_main_":
    jalankan_kalkulator()


**2. Menjalankan Program Kalkulator**
Untuk menjalankan kalkulator ini, ikuti langkah-langkah berikut:
Simpan kode di atas dalam file dengan nama kalkulator.py.
Buka terminal atau command prompt.
Navigasikan ke folder tempat file kalkulator.py disimpan.
Jalankan perintah berikut:
**python kalkulator.py**
Anda akan melihat menu kalkulator dan bisa mulai melakukan operasi matematika.
