# Praktikum 2 - Pemrograman Web
### Frans Putra Sinaga - 312210046
### TI.22.A1

## LANGKAH 1
buat dokumen html dengan isi berikut :
![s1](https://github.com/namasayafrans/Lab2Web/assets/115770839/5c357fd0-4369-46d0-8771-1ec510b8e862)

0```
<!DOCTYPE html>
<html lang="en">
<head>
 <meta charset="UTF-8">
 <meta name="viewport" content="width=device-width, initial-scale=1.0">
 <title>CSS Dasar</title>
</head>
<body>
 <header>
 <h1>CSS Internal dan <i>Inline CSS</i></h1>
 </header>
 <nav>
 <a href="lab2_css_dasar.html">CSS Dasar</a>
 <a href="lab2_css_eksternal.html">CSS Eksternal</a>
 <a href="lab1_tag_dasar.html">HTML Dasar</a>
 </nav>
 <!-- CSS ID Selector -->
 <div id="intro">
 <h1>Hello World</h1>
 <p>Kami sedang belajar HTML dan CSS dasar, pada mata kuliah <b>Pemrograman
Web</b> di <i>Universitas Pelita Bangsa</i>. Pelajaran pertama yang kami dapat
adalah membuat tampilan web sederhana dalam rangka mengenal tag-tag dasar HTML
dan CSS.</p>
 <!-- CSS Class Selector -->
 <a class="button btn-primary" href="#intro">Informasi selengkapnya.</a>
 </div>
</body>
</html>
```
lalu buka pada browser untuk melihat hasilnya
![step-1 output](https://i.imgur.com/o4JDDuV.png)
## LANGKAH 2
### Mendeklarasikan CSS Internal
Kemudian tambahkan deklarasi CSS internal seperti berikut pada bagian head dokumen
```
<head>
 <title>CSS Dasar</title>
 <style>
 body {
 font-family:'Open Sans', sans-serif;
 }
 header {
 min-height: 80px;
 border-bottom:1px solid #77CCEF;
 }
 h1 {
 font-size: 24px;
 color: #0F189F;
 text-align: center;
 padding: 20px 10px;
 }
 h1 i {
 color:#6d6a6b;
 }
 </style>
</head>
```
![step-2](https://i.imgur.com/74Emtig.png)

Selanjutnya simpan perubahan yang ada, dan lakukan refresh pada browser untuk melihat
hasilnya
![step-2 output](https://i.imgur.com/xVibmX4.png)

## LANGKAH 3
### Menambahkan Inline CSS
 tambahkan deklarasi inline CSS pada tag <p> seperti berikut
 ```
 <p style="text-align: center; color: #ccd8e4;">
 ```
 before:
 ![step-3 before](https://i.imgur.com/PdQFu6Z.png)
 after :
 ![step-3 after](https://i.imgur.com/ukibvhK.png)
 Simpan kembali dan refresh kembali browser untuk melihat perubahannya:

 ![step-3 output](https://i.imgur.com/WGGwbOZ.png)

 ## LANGKAH 4
 ### Membuat CSS Eksternal
 Buatlah file baru dengan nama style_eksternal.css kemudian buatlah deklarasi CSS seperti berikut
 ```
 nav {
background: #20A759;
color:#fff;
padding: 10px;
}
nav a {
color: #fff;
text-decoration: none;
padding:10px 20px;
}
nav .active,
nav a:hover {
background: #0B6B3A;
}
```
![step-4](https://i.imgur.com/ujFftw1.png)
Kemudian tambahkan tag `<link>`untuk merujuk file css yang sudah dibuat pada bagian `<head>`
```
<head>
 <!-- menyisipkan css eksternal -->
 <link rel="stylesheet" href="style_eksternal.css" type="text/css">
</head>
```
![step-4-1](https://i.imgur.com/W6UCxAk.png)

Selanjutnya refresh kembali browser untuk melihat perubahannya
![step-4-1](https://i.imgur.com/ISMBGGb.png)

## LANGKAH 5
### Menambahkan CSS Selector
Selanjutnya menambahkan CSS Selector menggunakan ID dan Class Selector. Pada file
style_eksternal.css, tambahkan kode berikut

```
/* ID Selector */
#intro {
background: #418fb1;
border: 1px solid #099249;
min-height: 100px;
padding: 10px;
}
#intro h1 {
text-align: left;
border: 0;
color: #fff;
}
/* Class Selector */
.button {
 padding: 15px 20px;
background: #bebcbd;
color: #fff;
display: inline-block;
margin: 10px;
text-decoration: none;
}
.btn-primary {
background: #E42A42;
}
```
![step-5](https://i.imgur.com/qcaS83z.png)
Kemudian simpan kembali dan refresh browser untuk melihat perubahannya.
![step-5 OUTPUT](https://i.imgur.com/gOklVYe.png)

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
