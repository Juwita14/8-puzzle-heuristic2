# 8-puzzle-heuristic2
Problem 8 puzzle akan diselesaikan dengan metode heuristic 2. 
c (x) = f (x) + h (x) di mana
    f (x) adalah panjang jalur dari root ke x
         (jumlah gerakan sejauh ini) dan
    h (x) adalah jumlah petak non-kosong yang tidak ada
         posisi tujuan mereka (jumlah mis-
         ubin yang ditempatkan). Setidaknya ada h (x)
         bergerak untuk mengubah keadaan x ke keadaan tujuan
         
![solve](https://user-images.githubusercontent.com/56763570/77401194-ba21ea80-6d69-11ea-870b-5990ef16a878.PNG)

Diatas adalah fungsi solve untuk menyelesaikan problem 8 puzzle. Difungsi tersebut pertama-tama membuat node untuk puzzle nya terlebih dahulu. Kemudian memanggil fungsi Calculate cost yang berguna untuk menghitung // Berfungsi untuk menghitung jumlah kotak tidak kosong yang tidak sesuai dengan posisi akhir.

![while](https://user-images.githubusercontent.com/56763570/77401947-0d486d00-6d6b-11ea-8a6d-43f77d71077c.PNG)

Untuk mencari nilai perpindahan yang paling sedikit. dan jika nilai min-> telah ditemukan yang paling kecil yaitu min->cost == 0 maka akan meng-outputkan hasilnya dengan memanggil fungsi printPath().
jika tidak maka blank space akan melakukan perpindahan lagi ke atas, bawah, kiri, atau kanan serta dihitung lagi costnya.

![safe](https://user-images.githubusercontent.com/56763570/77402475-f6564a80-6d6b-11ea-90c8-8d4da65bc9e9.PNG)

Dalam perpindahan blank space dibatasi oleh fungsi isSafe()
