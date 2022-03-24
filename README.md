# Praktikum 2 - Pemrograman Web

```
Maulana Hasanudin
312010106
TI.20.D.1
Universitas Pelita Bangsa
```

## LANGKAH 1
### Membuat dokumen HTML dengan nama file lab2_css_dasar.html. Setelah itu buat struktur dasar HTML dan masukan codingnya.
```
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
<img width="1070" alt="1" src="https://user-images.githubusercontent.com/101716660/159982432-764f913e-2263-4971-be08-24a6542704a8.png">

## LANGKAH 2

### Mendeklarasikan CSS Internal dibagian <head>.
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
<img width="1070" alt="2" src="https://user-images.githubusercontent.com/101716660/159982546-7b8b8204-a3a0-4374-9b9c-d41beab4e94b.png">

## LANGKAH 3
```
### menambahkan deklarasi Inline CSS pada tag <p>di bawah H1.
<p style="text-align: center; color: #ccd8e4;">
```
<img width="1070" alt="3" src="https://user-images.githubusercontent.com/101716660/159982732-7c75b536-4a06-4343-9cdf-b13fe9227977.png">

### LANGKAH 4
### Buat file baru dengan nama style_eksternal.css kemudian buat deklarasi CSS
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
<img width="1070" alt="4" src="https://user-images.githubusercontent.com/101716660/159982816-a0b72fb6-fe8f-4ee5-83af-50e3eb99d66d.png">

## LANGKAH 5
### tambahkan tag <link>untuk merujuk file css yang sudah dibuat pada bagian <head>padalab2_css_dasar.html
```
<head>
    <!-- menyisipkan css eksternal -->
    <link rel="stylesheet" href="style_eksternal.css" type="text/css">
</head>
```
<img width="1070" alt="5" src="https://user-images.githubusercontent.com/101716660/159982855-7bf87398-fe22-4f2f-b151-137b005e70a0.png">

## LANGKAH 6
### Tambahkan CSS Selector menggunakan ID dan Class Selector. pada filestyle_eksternal.css
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
<img width="1070" alt="6" src="https://user-images.githubusercontent.com/101716660/159982903-3297f500-b697-461a-ba20-6cf54f2ecd79.png">

#TUGAS
## 1. melakukan eksperimen dengan mengubah dan menambah properti dan nilai pada kode CSS dengan mengacu pada CSS Cheat Sheet yang diberikan pada file secara terpisah dari modul ini.
## Saya bereksperimen menambahkan latar belakang dan mengubah warna pada tombol
## TUGAS 1 CSS
<img width="1070" alt="7" src="https://user-images.githubusercontent.com/101716660/159982949-1e158c44-36d5-4537-b545-cef371615f93.png">

## 2. Apa perbedaan pendeklarasian CSS element h1 {...} dengan #intro h1 {...}? berikan penjelasannya!
Pendeklarasian CSS element h1 mengubah tampilan seluruh elemen yang memiliki tag h1, jika #intro h1 hanya mengubah tampilan elemen h1 yang memiliki id #intro.
## 3. Jika deklarasi CSS secara internal, maka ditambahkan CSS eksternal dan CSS inline pada elemen yang sama. apakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya!
jika mendeklarasikan CSS pada elemen yang sama namun isi deklarasinya berbeda, maka semua deklarasi CSS tersebut akan ditampilkan.
<img width="1070" alt="8" src="https://user-images.githubusercontent.com/101716660/159983039-99e97603-9c23-485e-87d3-046a76f88475.png">
<img width="1070" alt="9" src="https://user-images.githubusercontent.com/101716660/159983093-5ca92a20-2b94-41df-aab7-74407fc4fea3.png">

## 4. Pada sebuah elemen HTML terdapat ID dan Class, apabila masing-masing pemilih terdapat deklarasi CSS tersebut, maka deklarasi yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya!( < p  id = "paragraf-1"  class = "text-paragraf" > )
Kedua deklarasi tersebut akan tampil
  <img width="1070" alt="10" src="https://user-images.githubusercontent.com/101716660/159984003-c5f92e51-ed55-429b-a207-5b8bb5cb6c06.png">

  <img width="1070" alt="11" src="https://user-images.githubusercontent.com/101716660/159984216-1959c2e5-acbb-45a2-ab49-e3e94d67de0c.png">
