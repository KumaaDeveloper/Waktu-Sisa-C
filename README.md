# General
Simple C code to code a distance and remaining time program
  
## Code
```php
#include <stdio.h>

int main() {

    int jamPergi, menitPergi, detikPergi; // Waktu keberangkatan
    int jamJalan, menitJalan, detikJalan; // Waktu tempuh
    int totalJam, totalMenit, totalDetik; // Variabel untuk menyimpan total waktu

    // Menampilkan header untuk waktu keberangkatan
    printf("-------------------------\n");
    printf("|\tWaktu Pergi\t|\n");
    printf("-------------------------\n");

    // Menginput waktu keberangkatan
    printf("Pergi Jam Berapa?: ");
    scanf("%d", &jamPergi); // Input jam keberangkatan
    printf("Menit Ke Berapa?: ");
    scanf("%d", &menitPergi); // Input menit keberangkatan
    printf("Detik Ke Berapa?: ");
    scanf("%d", &detikPergi); // Input detik keberangkatan

    // Menampilkan header untuk waktu tempuh
    printf("\n-------------------------\n");
    printf("|\tWaktu Tempuh\t|\n");
    printf("-------------------------\n");

    // Menginput waktu tempuh
    printf("\nMenempuh Berapa Jam Di Jalan?: ");
    scanf("%d", &jamJalan); // Input jam tempuh
    printf("Menempuh Berapa Menit Di Jalan?: ");
    scanf("%d", &menitJalan); // Input menit tempuh
    printf("Menempuh Berapa Detik Di Jalan?: ");
    scanf("%d", &detikJalan); // Input detik tempuh

    // Menghitung total detik
    totalDetik = (detikPergi + detikJalan);
    int sisaDetik = totalDetik % 60; // Menghitung sisa detik setelah dibagi 60

    // Menghitung total menit
    totalMenit = (menitPergi + menitJalan + totalDetik / 60);
    int sisaMenit = totalMenit % 60; // Menghitung sisa menit setelah dibagi 60

    // Menghitung total jam
    totalJam = (jamPergi + jamJalan + totalMenit / 60);
    int sisaJam = totalJam % 24; // Menghitung sisa jam setelah dibagi 24

    // Menampilkan hasil waktu perjalanan
    printf("Maka pak synyster akan menempuh waktu perjalanan selama: %d jam, %d menit, %d detik\n", jamJalan, menitJalan, detikJalan);
    printf("Dan pak synyster akan sampai di tempat tujuan pada jam %d menit ke-%d detik ke-%d\n", sisaJam, sisaMenit, sisaDetik);
    
    return 0;
}
```
