# Praktikum 2 - Pemrograman Web
### Frans Putra Sinaga - 312210046
### TI.22.A1

## LANGKAH 1
buat dokumen html dengan isi berikut :
![s1](https://github.com/namasayafrans/Lab2Web/assets/115770839/5c357fd0-4369-46d0-8771-1ec510b8e862)
hasil ouput 
![s2](https://github.com/namasayafrans/Lab2Web/assets/115770839/5d60c1c8-49b1-4149-924d-f63c37c2e76f)

## LANGKAH 2
### Mendeklarasikan CSS Internal
Kemudian tambahkan deklarasi CSS internal seperti berikut pada bagian head dokumen
![s3](https://github.com/namasayafrans/Lab2Web/assets/115770839/1342cad3-c568-42d9-86f7-5e5c3fdba88b)
hasil ouput 
![s5](https://github.com/namasayafrans/Lab2Web/assets/115770839/8670f4d5-81d6-4a2f-968a-ca4743e783c1)

## LANGKAH 3
### Menambahkan Inline CSS
tambahkan deklarasi inline CSS pada tag <p> seperti berikut
![s4 1](https://github.com/namasayafrans/Lab2Web/assets/115770839/c39b59f5-4386-4120-876a-b4b7fcdb31ab)
hasil ouput 
![s4](https://github.com/namasayafrans/Lab2Web/assets/115770839/80299d4a-4583-4a0e-9cfe-80fbe5cef44a)

## LANGKAH 4
### Membuat CSS Eksternal
Buatlah file baru dengan nama style_eksternal.css kemudian buatlah deklarasi CSS seperti berikut
![s6](https://github.com/namasayafrans/Lab2Web/assets/115770839/7ce261bb-bc81-4b13-90e1-6023f5e108bf)
Di dalam file Lab2_css_eksternal.html 
![s7](https://github.com/namasayafrans/Lab2Web/assets/115770839/f8e4fb6c-0b0b-40a6-a98f-2c7b39681183)
hasil ouput 
![s8](https://github.com/namasayafrans/Lab2Web/assets/115770839/eb119efb-2156-43d3-a62b-f4f21bfa7fd9)

## LANGKAH 5
### Menambahkan CSS Selector
Selanjutnya menambahkan CSS Selector menggunakan ID dan Class Selector. Pada file style_eksternal.css, tambahkan kode berikut
![s9](https://github.com/namasayafrans/Lab2Web/assets/115770839/b5ccb52f-ada8-43d0-b179-d8a6843f9705)

Kemudian simpan kembali dan refresh browser untuk melihat perubahannya.
![s10](https://github.com/namasayafrans/Lab2Web/assets/115770839/7c542a65-b730-43a5-8d55-54191af3dfed)


# Pertanyaan dan Tugas
### 1. Lakukan eksperimen dengan mengubah dan menambah properti dan nilai pada kode CSS dengan mengacu pada CSS Cheat Sheet yang diberikan pada file terpisah dari modul ini
![step-6](https://i.imgur.com/sVetc6i.png)

### 2. Apa perbedaan pendeklarasian CSS elemen h1 {...} dengan #intro h1 {...}? berikan penjelasannya!
perbedaaannya jika hanya h1{} maka akan merubah semua yang ada didalam elemen h1 sedangkan intro h1 hanya akan merubah yang memiliki tag intro

### 3. Apabila ada deklarasi CSS secara internal, lalu ditambahkan CSS eksternal dan inline CSS pada elemen yang sama. Deklarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya!
jika ketiga CSS merubah elemen yang sama maka deklarasi tersebut akan mengikuti aturan prioritas
dimana prioritas CSS nya seperti ini:
1. inline CSS
2. ID selector CSS
3. internal CSS
4. external CSS

contoh:

ini adalah tampilan coding pada html testing dimana terdapat 2 kalimat yang memiliki elemen yang sama yaitu h1:
 ![step-7](https://i.imgur.com/87FHIwI.png)

 disini bisa dilihat sudah terdapat 2 css mencoba merubah warna text h1 :
 ![step-8](https://i.imgur.com/6BKuHMb.png) 

 sedangkan eksternal css berupa :
 ![step-9](https://i.imgur.com/eciJnc8.png)

 dan hasil adalah :
 ![step-10](https://i.imgur.com/THSnM36.png)
jadi saya mengambil kesimpulan bahwa semakin spesifik CSS tersebut maka prioritas semakin tinggi

### 4. Pada sebuah elemen HTML terdapat ID dan Class, apabila masing-masing selector tersebut terdapat deklarasi CSS, maka deklarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya! ( <p id="paragraf-1" class="text-paragraf"> )
hasilnya sesuai dengan kesimpulan saya sebelumnya semakin spesifik css tersebut maka akan semakin tinggi prioritas css tersebut
![step-11](https://i.imgur.com/eDobCFm.png)
disitu bisa dilihat terdapat 2 css yang merujuk ke elemen yang sama tapi 1 merujuk dengan id yang birisi font 40 dan warna emas sedangkan yang satu lagi merujuk dengan class yang berisi font 10 dan warna maroon
hasilnya adalah:
![step11-output](https://i.imgur.com/6wMF3Nt.png)
text "testing" tersebut mengikuti css selector id daripada selector class dikarenakan id lebih spesifik daripada class
