# Lab4Web

# Praktikum 4

# Pemograman WEB

~~~
Nama  : Isnaini Rizkyana
NIM   : 311910254
Kelas : TI.19.C1
~~~

## Langkah-langkah Praktikum
Persiapan membuat dokumen HTML dengan nama file lab4_box.html seperti berikut.
~~~
<!DOCTYPE html>
<html lang="en">
<head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>Box Element</title>
</head>
<body>
      <header>
          <h1>Box Element</h1>
      </header>
</body>
</html>
~~~

## Membuat Box Element
Kemudian tambahkan kode untuk membuat box element dengan tag div seperti berikut.
~~~
<section>
    <div class="div1">Div 1</div>
    <div class="div2">Div 2</div>
    <div class="div3">Div 3</div>
</section>
~~~
## CSS Float Property
Selanjutnya tambahkan deklarasi CSS pada head untuk membuat float element, seperti berikut.
~~~
<style>
  div {
    float:left;
    padding: 10px;
  }
  .div1 {
    background: red;
  }
  .div2 {
    background: yellow;
  }
  .div3 {
    background: green;
  }
</style>
~~~
![Membuat Element Box](https://user-images.githubusercontent.com/81541764/115877020-3016ea80-a471-11eb-8884-d841b3aa555e.JPG)

## Mengatur Clearfix Element
Clearfix digunakan untuk mengatur element setelah float element. Property clear digunakan untuk mengaturnya.

Tambahkan element div lainnya seteleah div3 seperti berikut.
~~~
<section>
      <div class="div1">Div 1</div>
      <div class="div2">Div 2</div>
      <div class="div3">Div 3</div>
      <div class="div4">Div 4</div>
</section>
~~~
Kemudian atur property clear pada CSS, seperti berikut.
~~~
.div4 {
    background-color: blue;
    clear: left;
    float: none;
}
~~~
![Mengatur Clearfix Element](https://user-images.githubusercontent.com/81541764/115877408-9a2f8f80-a471-11eb-8fe8-1b0b7278ff53.JPG)
Lakukan eksperimen terhadap penggunaan property clear dengan nilai lainnya (left, both, right), dan amati perubahannya.

## Membuat Layout Sederhana
Kita akan membuat layout web sederhana seperti gambar berikut.

![A](https://user-images.githubusercontent.com/81541764/115877832-132ee700-a472-11eb-8736-6d3c7ad73903.JPG)

### Buat folder baru dengan nama lab4_layout, kemudian buatlah file baru didalamnya dengan nama home.html, dan file css dengan nama style.css.
~~~
<!DOCTYPE html>
<html lang="en">
<head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>Layout Sederhana</title>
      <link rel="stylesheet" href="style.css">
</head>
<body>
      <div id="container">

      </div>
</body>
</html>
~~~
Kemudian buat kerangka layout dengan semantics element seperti berikut.
![semantic element](https://user-images.githubusercontent.com/81541764/115878269-8df80200-a472-11eb-90d4-8f675b490a5c.JPG)

Kemudian tulis kode berikut.
~~~
<header>
      <h1>Layout Sederhana</h1>
</header>
<nav>
      <a href="home.html" class="active">Home</a>
      <a href="artikel.html">Artikel</a>
      <a href="about.html">About</a>
      <a href="kontak.html">Kontak</a>
</nav>
<section id="hero"></section>
<section id="wrapper">
      <section id="main"></section>
      <aside id="sidebar"></aside>
</section>
<footer>
      <p>&copy; 2021 - Universitas Pelita Bangsa</p>
</footer>
~~~
Kemudian buka browser dan lihat hasilnya.

![Membuat Layout Sederhana](https://user-images.githubusercontent.com/81541764/115878683-0363d280-a473-11eb-8dc0-e43356331ae7.JPG)

Kemudian tambahkan kode CSS untuk membuat layoutnya.
~~~
/* import google font */
@import
url('https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300;0,
400;0,600;0,700;0,800;1,300;1,400;1,600;1,700;1,800&display=swap');
@import
url('https://fonts.googleapis.com/css2?family=Open+Sans+Condensed:ital,
wght@0,300;0,700;1,300&display=swap');
/* Reset CSS */ * {
      margin: 0; padding: 0;
}
body {
      line-height:1;
      font-size:100%;
      font-family:'Open Sans', sans-serif;
      color:#5a5a5a;
}
#container {
      width: 980px;
      margin: 0 auto;
      box-shadow: 0 0 1em #cccccc;
}
/* header */
header {
      padding: 20px;
}
header h1 {
      margin: 20px 10px;
      color: #b5b5b5;
}
~~~


