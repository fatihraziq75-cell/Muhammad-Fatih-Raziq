# Muhammad-Fatih-Raziq
Tugas Dasar Pemrograman P1

Penjelasan mengenai program tersebut yang dimulai dengan pemenuhan kriteria tugas: 
1. Mengambil 3 input terminal dari nama, minuman favorit, dan umur.
2. Menghasilkan ID yang unik minimal 10 karakter kombinasi huruf dan angka.
3. Menggunakan fungsi sprintf() untuk konkatenasi string dan mencakup minimal 2 operasi matematika.
4. Hanya menggunakan library standar #include <stdio.h>.

Lalu, bagaimana cara kerjanya?

Pertama, scanf() membaca input string dan integer dari terminal. Setelah dibaca, akses karakter array akan mengambil huruf pertama nama, dan mengambil nama dari huruf ke-4. Setelah itu, sprintf(id, ...) mengonversi angka dan menggabungkan berbagai tipe data (karakter dan angka) menjadi satu variabel string tanpa perlu mencetak langsung ke layar dan terakhir menggunakan printf() untuk menampilkan format tulisan yang sesuai.



#include <stdio.h>

int main() {
    char nama[50];
    char favorite_drink[50];
    int umur;
    char id[100];

    // 1. Mengambil input dari pengguna
    printf("Masukkan Nama: ");
    scanf("%s", nama);

    printf("Masukkan Favorite Drink: ");
    scanf("%s", favorite_drink);

    printf("Masukkan Umur: ");
    scanf("%d", &umur);

    // Menghitung komponen ID berdasarkan formula di contoh
    char inisial_nama = nama[0];                                // Inisial nama (misal 'A')
    int operasi1 = (1000 - umur) + umur;                       // Operasi 1
    int ASCII_M = 'M';                                         // Nilai ASCII 'M' (77)
    int ASCII_m = 'm';                                         // Nilai ASCII 'm' (109)
    int operasi2 = ASCII_M + ASCII_m;                          // Operasi 2 (77 + 109 = 186)
    char inisial_drink = favorite_drink[0];                    // Inisial minuman (misal 'M')
    char akhiran_nama = nama[3];                               // Karakter ke-4/akhiran nama (misal 's')

    // 2. Menggabungkan (konkatenasi) menggunakan sprintf()
    sprintf(id, "%c%d%d%c%c", inisial_nama, operasi1, operasi2, inisial_drink, akhiran_nama);

    // 3. Menampilkan Output Kartu ID
    printf("\n--------------------------------------------------\n");
    printf("| ID            : %s\n", id);
    printf("| Name          : %s\n", nama);
    printf("| Favorite Food : Nasi Padang\n");
    printf("--------------------------------------------------\n");

    return 0;
}

<img width="428" height="122" alt="WhatsApp Image 2026-09-29 at 02 57 30" src="https://github.com/user-attachments/assets/e4b3eae4-7106-42f4-a064-48b7799e699e" />
