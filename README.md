# 8-puzzle-heuristic2
Problem 8 puzzle akan diselesaikan dengan metode heuristic 2. 
c (x) = f (x) + h (x) di mana
f (x) adalah panjang jalur dari root ke x(jumlah gerakan sejauh ini) dan
h (x) adalah jumlah kotak non-kosong yang tidak ada posisi tujuan mereka. Setidaknya ada h (x) bergerak untuk mengubah keadaan x ke keadaan tujuan
<br/>![prioryty](https://user-images.githubusercontent.com/56763570/78731460-a2fc0480-78f4-11ea-881b-3d3fc22f6d9f.PNG)<br/>
fungsi c (x) di program ini berada di struct comp yang akan menjadi standar priority pemilihan tahapan 8 puzzle berikutnya.
         
![solve](https://user-images.githubusercontent.com/56763570/77401194-ba21ea80-6d69-11ea-870b-5990ef16a878.PNG)

Diatas adalah fungsi solve untuk menyelesaikan problem 8 puzzle. Difungsi tersebut pertama-tama membuat node untuk puzzle nya terlebih dahulu. Kemudian memanggil fungsi Calculate cost yang berguna untuk menghitung jumlah kotak tidak kosong yang tidak sesuai dengan posisi akhir.

![while](https://user-images.githubusercontent.com/56763570/77401947-0d486d00-6d6b-11ea-8a6d-43f77d71077c.PNG)

Untuk mencari nilai perpindahan yang paling sedikit. dan jika nilai min->cost telah ditemukan yang paling kecil yaitu min->cost == 0 (yang berarti puzzle telah sesuai dengan posisi akhir yang telah ditentukan) maka akan meng-outputkan hasilnya dengan memanggil fungsi printPath().

![print](https://user-images.githubusercontent.com/56763570/77402876-9318e800-6d6c-11ea-8862-82db85ceda53.PNG)

jika tidak maka blank space akan melakukan perpindahan lagi ke atas, bawah, kiri, atau kanan serta dihitung lagi costnya.

![safe](https://user-images.githubusercontent.com/56763570/77402475-f6564a80-6d6b-11ea-90c8-8d4da65bc9e9.PNG)

Dalam perpindahan blank space dibatasi oleh fungsi isSafe()
