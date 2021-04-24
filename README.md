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
Kemudian lihat hasilnya pada browser.

![Membuat Layout Sederhana2](https://user-images.githubusercontent.com/81541764/115881211-bb927a80-a475-11eb-92d7-5a833e772696.JPG)

## Membuat Navigasi
Kemudian selanjutnya mengatur navigasi.
~~~
/* navigasi */
nav {
      display: block;
      background-color: #1f5faa;
}
nav a {
      padding: 15px 30px;
      display: inline-block;
      color: #ffffff;
      font-size: 14px;
      text-decoration: none;
      font-weight: bold;
}
nav a.active, nav a:hover {
      background-color: #2b83ea;
}
~~~
Kemudian lihat hasilnya.

![Membuat Navigasi](https://user-images.githubusercontent.com/81541764/115881544-0d3b0500-a476-11eb-97d0-cc9eae09c1cf.JPG)

## Membuat Hero Panel.
Selanjutnya membuat hero panel. Tambahkan kode HTML dan CSS seperti berikut.
~~~
<section id="hero">
      <h1>Hello World!</h1>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem elit, iaculis innisl volutpat,
      malesuada tincidunt arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer pharetra est nunc,
      nec pretium nunc pretium ac.</p> <a href="home.html" class="btn btn-large">Learn more &raquo;</a>
</section>
~~~
~~~
/* Hero Panel */
#hero {
      background-color: #e4e4e5;
      padding: 50px 20px;
      margin-bottom: 20px;
}
#hero h1 {
      margin-bottom: 20px;
      font-size: 35px;
}
#hero p {
      margin-bottom: 20px;
      font-size: 18px;
      line-height: 25px;
}
~~~

![Membuat Hero Panel](https://user-images.githubusercontent.com/81541764/115881892-6b67e800-a476-11eb-84ed-948b621d8b45.JPG)

## Mengatur Layout Main dan Sidebar
Selanjutnya mengatur main content dan sidebar, tambahkan CSS float.
~~~
/* main content */
#wrapper {
      margin: 0;
}
#main {
      float: left;
      width: 640px;
      padding: 20px;
}
/* sidebar area */
#sidebar {
      float: left;
      width: 260px;
      padding: 20px;
}
~~~

## Membuat Sidebar Widget
Kemudian selanjutnya menambahkan element lain dalam sidebar.
~~~
<aside id="sidebar">
      <div class="widget-box">
            <h3 class="title">Widget Header</h3>
            <ul>
                  <li><a href="#">Widget Link</a></li>
                  <li><a href="#">Widget Link</a></li>
                  <li><a href="#">Widget Link</a></li>
                  <li><a href="#">Widget Link</a></li>
                  <li><a href="#">Widget Link</a></li>
            </ul>
      </div>
      <div class="widget-box">
            <h3 class="title">Widget Text</h3>
            <p>Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla,
            vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc pretium ac.</p>
      </div>
</aside>
~~~
Kemudian tambahkan CSS.
~~~
/* widget */
.widget-box {
      border:1px solid #eee;
      margin-bottom:20px;
}
.widget-box .title {
      padding:10px 16px;
      background-color:#428bca;
      color:#fff;
}
.widget-box ul {
      list-style-type:none;
}
.widget-box li {
      border-bottom:1px solid #eee;
}
.widget-box li a {
      padding:10px 16px;
      color:#333;
      display:block;
      text-decoration:none;
}
.widget-box li:hover a {
      background-color:#eee;
}
.widget-box p {
      padding:15px; line-height:25px;
}
~~~

![Membuat Sidebar Widget](https://user-images.githubusercontent.com/81541764/115883206-bc2c1080-a477-11eb-82c7-d4264a4513a0.JPG)

## Mengatur Footer
Selanjutnya mengatur tampilan footer. Tambahkan CSS untuk footer.
~~~
/* footer */
footer {
      clear:both;
      background-color:#1d1d1d;
      padding:20px;
      color:#eee;
}
~~~

![Mengatur Footer](https://user-images.githubusercontent.com/81541764/115883679-407e9380-a478-11eb-9eed-8064d5f33069.JPG)

## Menambahkan Elemen lainnya pada Main Content
~~~
<section id="main">
            <div class="row">
                <div class="box">
                    <img src="https://dummyimage.com/120/db7d25/fff.png" alt="" class="image-circle">
                    <h3>Heading</h3>
                    <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
                    <a href="#" class="btn btn-default">View detail</a>
                </div>
                <div class="box">
                    <img src="https://dummyimage.com/120/3e73e6/fff.png" alt="" class="image-circle">
                    <h3>Heading</h3>
                    <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
                    <a href="#" class="btn btn-default">View detail</a>
                </div>
                <div class="box">
                    <img src="https://dummyimage.com/120/71e6d4/fff.png" alt="" class="image-circle">
                    <h3>Heading</h3>
                    <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
                    <a href="#" class="btn btn-default">View detail</a>
                </div>
            </div>
</section>
~~~

Kemudian tambahkan CSS.
~~~
/* box */
    .box {
        display:block;
        float:left;
        width:33.333333%;
        box-sizing:border-box;
        -moz-box-sizing:border-box;
        -webkit-box-sizing:border-box;
        padding:0 10px;
        text-align:center;
    }
    .box h3 {
        margin: 15px 0;
    }
    .box p {
        line-height: 20px;
        font-size: 14px;
        margin-bottom: 15px;
    }
    box img {
        border: 0;
        vertical-align: middle;
    }
    .image-circle {
        border-radius: 50%;
    }
    .row {
        margin: 0 -10px;
        box-sizing: border-box;
        -moz-box-sizing: border-box;
        -webkit-box-sizing: border-box;
    }
    .row:after, .row:before, .entry:after, .entry:before {
        content:'';
        display:table;
    }
    .row:after, .entry:after {
        clear:both;
    }
~~~

Lihat hasilnya dibrowser.

![Menambahkan Elemen lainnya pada Main Content](https://user-images.githubusercontent.com/81541764/115920422-5d30c080-a4a4-11eb-91fa-cba26df6dd27.JPG)

## Menambahkan Content Artikel
Selanjutnya membuat content artikel. Tambahkan HTML berikut pada main content.
~~~
        <hr class="divider" />
            <article class="entry">
                <h2>First featurette heading.</h2>
                <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="">
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem elit,
                    iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla, vestibulum mi porta,
                    faucibus felis. Integer pharetra est nunc, nec pretium nunc pretium ac.</p>
            </article>
        <hr class="divider" />
            <article class="entry">
                <h2>First featurette heading.</h2>
                <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="" class="right-img">
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem elit,
                    iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla, vestibulum mi porta,
                    faucibus felis. Integer pharetra est nunc, nec pretium nunc pretium ac.</p>
            </article>
~~~
Kemudian tambahkan CSS.
~~~
.divider {
        border:0;
        border-top:1px solid #eeeeee;
        margin:40px 0;
    }
    /* entry */
    .entry {
        margin: 15px 0;
    }
    .entry h2 {
        margin-bottom: 20px;
    }
    .entry p {
        line-height: 25px;
    }
    .entry img {
        float: left;
        border-radius: 5px;
        margin-right: 15px;
    }
    .entry .right-img {
        float: right;
    }
~~~

![Menambahkan Content Artikel](https://user-images.githubusercontent.com/81541764/115920665-b567c280-a4a4-11eb-9dc7-15ec6e160cad.JPG)

## Pertanyaan dan Tugas
1. Tambahkan Layout untuk menu About
=> buat single layout yang berisi deskripsi, portfolio, dll

Persiapan membuat dokumen HTML dengan nama file about.html seperti berikut.
~~~
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Tentang</title>
        <link rel="stylesheet" href="style.css">
    </head>
    <body>
        <div id="container">
        <header>
            <h1>Layout Sederhana</h1>
        </header>
        <nav>
            <a href="home.html" class="active">Home</a>
            <a href="artikel.html">Artikel</a>
            <a href="about.html">About</a>
            <a href="kontak.html">Kontak</a>
        </nav>
        <section id="hero1">
            <h1>Tentang</h1>
            <p>Saya Isnaini Rizkyana lahir di Bekasi 5 Mei 1997 usia 23 tahun.
                Saya adalah seorang mahasiswa Universitas Pelita Bangsa semester 4 mengambil prodi jurusan Teknik Informatika.
            </p>
            <br>
            <br>
            <h1>Portofolio</h1>
            <img src="isnaini.png" style="width:950px;height:1200px;">
        </section>
        <footer>
            <p>&copy; 2021 - Universitas Pelita Bangsa</p>
        </footer>
        </div>
    </body>
</html>
~~~
Kemudian buka browser dan lihat hasilnya.

![tentang](https://user-images.githubusercontent.com/81541764/115945740-38117180-a4e7-11eb-8e9c-f246bc6752e8.JPG)

2. Tambahkan layout untuk menu Contact
=> yang berisi form isian: nama, email, message, dll

Persiapan membuat dokumen HTML dengan nama file kontak.html seperti berikut.
~~~
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Kontak</title>
        <link rel="stylesheet" href="style.css">
    </head>
    <body>
        <div id="container">
        <header>
            <h1>Layout Sederhana</h1>
        </header>
        <nav>
            <a href="home.html" class="active">Home</a>
            <a href="artikel.html">Artikel</a>
            <a href="about.html">About</a>
            <a href="kontak.html">Kontak</a>
        </nav>
<body>
    <section id="wrapper">
        <section id="main">
        <div class="row">
            <div class="box">
                <img src="" alt="" class="">
                <h3></h3>
                <p></p>
                <a href="#" class="btn btn-default"></a>
            </div>
        </div>
    <hr class="divider" />
        <article class="entry">
            <h2></h2>
            <img src="" alt="">
            <p>
                <form action="" method="POST">
                    <fieldset>
                    <legend>Contact</legend>
                    <p>
                        <label>Name     :       Isnaini Rizkyana</label>
                    </p>
                    <br>
                    <p>
                        <label>Email    :       Isnainirizkyana55@gmail.com</label>
                    </p>
                    <br>
                    <p>
                        <label>Message  :       Jangan pernah putus asa dan teruslah berusaha</label>
                    </p>
                    </fieldset>
            </p>
        </article>
    <hr class="divider" />
        <article class="entry">
            <h2></h2>
            <img src="" alt="" class="">
            <p></p>
        </article>
    </section>
        <aside id="">
            <div class="">
                <h3 class=""></h3>
                <ul>
                </ul>
            </div>
            <div class="">
                <h3 class=""></h3>
                <p></p>
            </div>
        </aside>
    </section> 
    <footer>
        <p>&copy; 2021 - Universitas Pelita Bangsa</p>
    </footer>
</body>
</html>
~~~
Kemudian buka browser dan lihat hasilnya.
![kontak](https://user-images.githubusercontent.com/81541764/115945809-8a529280-a4e7-11eb-840d-f1e6ef6fd7db.JPG)

