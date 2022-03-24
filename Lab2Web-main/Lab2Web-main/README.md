# Praktikum 2 - Pemrograman Web
```
Veno Setyoaji Wiratama
311910363
TI.19.A.2
Universitas Pelita Bangsa
```

## LANGKAH 1
### Membuat dokumen HTML dengan nama file lab2_css_dasar.html. Setelah itu buat struktur dasar HTML dan masukan coding nya.
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
![LANGKAH 1](https://user-images.githubusercontent.com/22215113/115101856-9e3f4700-9f71-11eb-9409-0c1cdecad523.png)

## LANGKAH 2
### Mendeklarasikan CSS Internal dibagian `<head>`.
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
![LANGKAH 2](https://user-images.githubusercontent.com/22215113/115101859-a303fb00-9f71-11eb-82fc-332e23d870e8.png)

## LANGKAH 3
### Menambahkan deklarasi Inline CSS pada tag `<p>` dibawah H1.
```
<p style="text-align: center; color: #ccd8e4;">
```
![LANGKAH 3](https://user-images.githubusercontent.com/22215113/115101862-a7301880-9f71-11eb-9662-f508b98a278d.png)

## LANGKAH 4
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
![LANGKAH 4](https://user-images.githubusercontent.com/22215113/115101866-ab5c3600-9f71-11eb-8b2b-c9d86b2129b2.png)

## LANGKAH 5
### Tambahkan tag `<link>` untuk merujuk file css yang sudah dibuat pada bagian `<head>` pada `lab2_css_dasar.html`
```
<head>
    <!-- menyisipkan css eksternal -->
    <link rel="stylesheet" href="style_eksternal.css" type="text/css">
</head>
```
![LANGKAH 5](https://user-images.githubusercontent.com/22215113/115101869-ae572680-9f71-11eb-9930-87d298b281c2.png)

## LANGKAH 6
### Tambahkan CSS Selector menggunakan ID dan Class Selector. Pada file `style_eksternal.css`
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
![LANGKAH 6](https://user-images.githubusercontent.com/22215113/115101872-b1eaad80-9f71-11eb-80f2-abf0973ab01d.png)

## TUGAS
### 1. Lakukan eksperimen dengan mengubah dan menambah properti dan nilai pada kode CSS dengan mengacu pada CSS Cheat Sheet yang diberikan pada file terpisah dari modul ini.
* Saya bereksperimen menambahkan background dan mengubah warna pada button
* ![TUGAS 1 CSS](https://user-images.githubusercontent.com/22215113/115101324-4d2d5400-9f6d-11eb-89f5-63b9f26c08c4.png)
* ![TUGAS 1](https://user-images.githubusercontent.com/22215113/115101321-47377300-9f6d-11eb-9104-68d3ed26a435.png)

### 2. Apa perbedaan pendeklarasian CSS elemen h1 {...} dengan #intro h1 {...}? berikan penjelasannya!
* Pendeklarasian CSS elemen h1 mengubah tampilan seluruh elemen yang memiliki tag h1, jika #intro h1 hanya mengubah tampilan elemen h1 yang memiliki id #intro.

### 3. Apabila ada deklarasi CSS secara internal, lalu ditambahkan CSS eksternal dan inline CSS pada elemen yang sama. Deklarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya!
* jika mendeklarasikan CSS pada elemen yang sama namun isi deklarasi nya berbeda, maka semua deklarasi CSS tersebut akan ditampilkan.
* ![TUGAS NO 3](https://user-images.githubusercontent.com/22215113/115101646-202e7080-9f70-11eb-922b-5ed2fafdd6c9.png)
* ![TUGAS NO 3 css](https://user-images.githubusercontent.com/22215113/115101472-ae095c00-9f6e-11eb-9c33-47a8c4f6cf66.png)

### 4. Pada sebuah elemen HTML terdapat ID dan Class, apabila masing-masing selector tersebut terdapat deklarasi CSS, maka deklarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya! `( <p id="paragraf-1" class="text-paragraf"> )`
* Kedua deklarasi tersebut akan tampil
* ![TUGAS NO 4](https://user-images.githubusercontent.com/22215113/115101693-887d5200-9f70-11eb-99be-24a7fe29f872.png)
* ![TUGAS NO 4 css](https://user-images.githubusercontent.com/22215113/115101692-874c2500-9f70-11eb-8c49-3d43cabd67f3.png)


