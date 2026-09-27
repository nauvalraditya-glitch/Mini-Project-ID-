# Mini-Project-ID
Nauval Raditya Pratama
5048261045

<img width="431" height="200" alt="Screenshot 2026-09-27 213047" src="https://github.com/user-attachments/assets/0df49817-4dc0-4e33-a712-a8670194c6dc" />

Output di atas dihasilkan dari 3 input menggunakan tipe data char dan int.
Di mana char berfungsi untuk menyimpan karakter dari nama dan hobi,
sedangkan int berfungsi untuk menyimpan bilangan bulat dari umur.
Operasi yang digunakan untuk menghasilkan ID adalah umur dikali 2 dan menggunakan jumlah dari kode ASCII dari huruf awal nama dan hobi.
Kode ini menggunakan sprintf, output dari sprintf ini tidak langsung ditampilkan di layar melainkan disimpan di variabel ID.

Penjelasan dari kode ID yang saya buat :
1. char [20] = menyimpan 20 karakter.
2.  %20[^\n] artinya "baca semua karakter yang bukan newline, maksimal 20 huruf", Spasi di depan (" %20...") berfungsi buat "membersihkan" sisa enter/newline yang mungkin masih nyangkut di buffer dari input sebelumnya.
3. nama[0] = menyimpan huruf awal dari nama dan berlaku untuk hobi juga.
4. menggunakan 2 operasi untuk menghasilkan id (umur + kode ASCII)
5. char id[11] = menyimpan id sebanyak 10, menggunakan 11 karena disiapkan buat nampung 10 karakter ID plus 1 slot buat karakter penutup otomatis ('\0') yang selalu ditambahkan C di akhir setiap string.
6. sprintf(id, "%c%04d%04d%c", inisialNama, umurKali2, jumlahAscii, inisialHobi); dari kode ini disimpan huruf awal nama + 4 digit bilangan dari operasi 1 + 4 digit bilangan dari operasi 2 + huruf awal hobi
