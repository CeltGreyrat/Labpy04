# LABPY04

## FLOWCHART
![Flowchart](Diagram_Nilai.png)

## Codingan
````python
def hitung_nilai_akhir(nilai_tugas_values, nilai_uts_values, nilai_uas_values):
    # Hitung Nilai Akhir Berdasarkan Nilai Rata-Rata 
    nilai_akhir = (nilai_tugas_values * 0.30) + (nilai_uts_values * 0.30) + (nilai_uas_values * 0.40)
    return nilai_akhir

# Daftar Untuk Menyimpan Data 
nama = []
nim = []
nilai_tugas = []
nilai_uts = []
nilai_uas = []
nilai_akhir_values = []

# Input Loop Untuk Mengumpulkan Data Mahasiswa
while True:
    nama_values = input("Nama: ")
    nim_values = input("NIM: ")
    nilai_tugas_values = float(input("Nilai Tugas: "))
    nilai_uts_values = float(input("Nilai UTS: "))
    nilai_uas_values = float(input("Nilai UAS: "))

    # Menghitung Nilai Akhir
    nilai_akhir = hitung_nilai_akhir(nilai_tugas_values, nilai_uts_values, nilai_uas_values)

    # Menambahkan Data Ke List
    nama.append(nama_values)
    nim.append(nim_values)
    nilai_tugas.append(nilai_tugas_values)
    nilai_uts.append(nilai_uts_values)
    nilai_uas.append(nilai_uas_values)
    nilai_akhir_values.append(round(nilai_akhir, 2))

    # Menambah Data
    tambah_data = input("Apakah Anda ingin menambah data lagi? (y/t): ").lower()
    if tambah_data == 't':
        break

# Output Untuk Data Yang Sudah Dikumpulkan
print("\nDaftar Mahasigma:")
print(f"{'Nama':<20} | {'NIM':<10} | {'Tugas':<10} | {'UTS':<10} | {'UAS':<10} | {'Nilai Akhir':<15}")
print("=" * 80)
for nama_values, nim_values, nilai_tugas_values, nilai_uts_values, nilai_uas_values, nilai_akhir_values in zip(nama, nim, nilai_tugas, nilai_uts, nilai_uas, nilai_akhir_values):
    print(f"{nama_values:<20} {nim_values:<10} {nilai_tugas_values:<10} {nilai_uts_values:<10} {nilai_uas_values:<10} {nilai_akhir_values:<15}")
````

## Output
````
nama : vito
nim : 5658
nilai tugas : 80
nilai uts : 70
nilai uas : 75
Apakah Anda ingin menambah data lagi? (y/t): y
nama : nopal
nim : 5758
nilai tugas : 90
nilai uts : 60
nilai uas : 65
Apakah Anda ingin menambah data lagi? (y/t): t

Daftar Mahasigma:
Nama                 | NIM        | Tugas      | UTS        | UAS        | Nilai Akhir
================================================================================
vito                 5658          80.0        70.0          75.0          67.5
nopal                5758          90.0        60.0          65.0          64.5
````

## Penjelasan

mengitung_nilai_akhir, menghitung nilai akhir dari semua nilai.
daftar_untuk_menyimpan_data, fungsi ini di tunjukan untuk menyimpan data dan jika ingin merubahnya hanya perlu memanggil variabel dari data ini.
input_loop_untuk_mengumpukan_data_mahasiswa, fungsi untuk melakukan looping.
menambahkan_data_ke_list, fungsi ini di gunakan untuk mengubah data di list.
menambah_data, memberikan pilihan jika memlilih 'y' maka user akan menambahkan data baru lagi dan jika memilih 't' maka seluruh fungsi akan berhenti dan akan memasuki tahap berikutnya
output_untuk_data_yang_sudah_dikumpulkan, fungsi untuk membuat tabel list dari sistem yang di atas.




