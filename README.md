# Lab4Web
# Muhamad Wafa Mufida Zulfi
# 312410334
# TI. 24. A4
#

Langkah-langkah Praktikum
Persiapan membuat dokumen HTML dengan nama file lab4_box.html seperti berikut:
```
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
````
Membuat Box Element
Kemudian tambahkan kode untuk membuat box element dengan tag <div> seperti berikut:

<section>
    <div class="div1">Div 1</div>
    <div class="div2">Div 2</div>
    <div class="div3">Div 3</div>
</section>
CSS Float Property
Selanjutnya tambahkan deklarasi CSS pada bagian <head> untuk membuat elemen float, seperti berikut:

<style>
    div {
        float: left;
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
Hasil codingan nya:

image
Mengatur Clearfix Element
Clearfix digunakan untuk mengatur elemen setelah float element. Property clear digunakan untuk mengatur posisi agar elemen berikutnya tidak sejajar dengan elemen yang difloat.

Tambahkan elemen <div> lainnya setelah div3 seperti berikut:

<section>
    <div class="div1">Div 1</div>
    <div class="div2">Div 2</div>
    <div class="div3">Div 3</div>
    <div class="div4">Div 4</div>
</section>
Kemudian atur property clear pada CSS seperti berikut:

.div4 {
    background-color: blue;
    clear: left;
    float: none;
}
Hasil di run di browser:

image
Membuat Layout Sederhana
Buat folder baru dengan nama lab4_layout, kemudian buat dua file di dalamnya:

home.html
style.css
Berikut struktur awal file home.html:

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
Kemudian buat kerangka layout dengan semantics element seperti berikut.

image
Kemudian tulis kode berikut:

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
Hasil di browser:

image
Kemudian tambahkan kode CSS untuk membuat layoutnya:

/* Import Google Font */
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300;0,400;0,600;0,700;0,800;1,300;1,400;1,600;1,700;1,800&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Open+Sans+Condensed:ital,wght@0,300;0,700;1,300&display=swap');

/* Reset CSS */
* {
    margin: 0;
    padding: 0;
}

/* Body */
body {
    line-height: 1;
    font-size: 100%;
    font-family: 'Open Sans', sans-serif;
    color: #5a5a5a;
}

/* Container */
#container {
    width: 980px;
    margin: 0 auto;
    box-shadow: 0 0 1em #cccccc;
}

/* Header */
header {
    padding: 20px;
}

header h1 {
    margin: 20px 10px;
    color: #b5b5b5;
}
Hasil saat di run di browser:

image
Membuat Navigasi
Kemudian selanjutnya mengatur navigasi.

/* Navigasi */
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

nav a.active,
nav a:hover {
    background-color: #2b83ea;
}
Hasil saat di run di browser

image
Membuat Hero Panel
Selanjutnya membuat hero panel. Tambahkan kode HTML dan CSS seperti berikut:

image
Mengatur Layout Main dan Sidebar
Selanjutnya mengatur main content dan sidebar, tambahkan CSS float berikut:

/* Main Content */
#wrapper {
    margin: 0;
}

#main {
    float: left;
    width: 640px;
    padding: 20px;
}

/* Sidebar Area */
#sidebar {
    float: left;
    width: 260px;
    padding: 20px;
}
Membuat Sidebar Widget
Kemudian selanjutnya menambahkan elemen lain dalam sidebar:

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
        <p>
            Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt
            arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer
            pharetra est nunc, nec pretium nunc pretium ac.
        </p>
    </div>
</aside>
Kemudian tambahkan CSS berikut:
/* Widget */
.widget-box {
    border: 1px solid #eee;
    margin-bottom: 20px;
}

.widget-box .title {
    padding: 10px 16px;
    background-color: #428bca;
    color: #fff;
}

.widget-box ul {
    list-style-type: none;
}

.widget-box li {
    border-bottom: 1px solid #eee;
}

.widget-box li a {
    padding: 10px 16px;
    color: #333;
    display: block;
    text-decoration: none;
}

.widget-box li:hover a {
    background-color: #eee;
}

.widget-box p {
    padding: 15px;
    line-height: 25px;
}
Hasil tampilan di browser nya:
image
Mengatur Footer
Selanjutnya mengatur tampilan footer. Tambahkan CSS untuk footer:

/* Footer */
footer {
    clear: both;
    background-color: #1d1d1d;
    padding: 20px;
    color: #eee;
}
Hasil di tampilan browsernya:
image
Menambahkan Elemen lainnya pada Main Content:
<section id="main">
    <div class="row">

        <div class="box">
            <img src="https://dummyimage.com/120/db7d25/fff.png" alt="" class="image-circle">
            <h3>Heading</h3>
            <p>
                Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.
            </p>
            <a href="#" class="btn btn-default">View detail</a>
        </div>

        <div class="box">
            <img src="https://dummyimage.com/120/3e73e6/fff.png" alt="" class="image-circle">
            <h3>Heading</h3>
            <p>
                Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.
            </p>
            <a href="#" class="btn btn-default">View detail</a>
        </div>

        <div class="box">
            <img src="https://dummyimage.com/120/71e6d4/fff.png" alt="" class="image-circle">
            <h3>Heading</h3>
            <p>
                Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.
            </p>
            <a href="#" class="btn btn-default">View detail</a>
        </div>

    </div>
</section>
Kemudian tambahkan CSS:
/* box */
.box {
    display: block;
    float: left;
    width: 33.333333%;
    box-sizing: border-box;
    -moz-box-sizing: border-box;
    -webkit-box-sizing: border-box;
    padding: 0 10px;
    text-align: center;
}

.box h3 {
    margin: 15px 0;
}

.box p {
    line-height: 20px;
    font-size: 14px;
    margin-bottom: 15px;
}

.box img {
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

.row:after, 
.row:before,
.entry:after, 
.entry:before {
    content: '';
    display: table;
}

.row:after,
.entry:after {
    clear: both;
}
Hasil saat tampilan di browser
image
Menambahkan Content Artikel:
<hr class="divider" />

<article class="entry">
    <h2>First featurette heading.</h2>
    <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="">
    <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem elit, 
        iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla, 
        vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc 
        pretium ac.
    </p>
</article>

<hr class="divider" />

<article class="entry">
    <h2>First featurette heading.</h2>
    <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="" class="right-img">
    <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem elit, 
        iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla, 
        vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc 
        pretium ac.
    </p>
</article>
Kemudian tambahkan CSS:
.divider {
    border: 0;
    border-top: 1px solid #eeeeee;
    margin: 40px 0;
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
Hasil tampilan di browser nya:
screencapture-127-0-0-1-5500-lab4-layout1-html-2025-10-17-00_16_47
Pertanyaan dan tugas:
image
Tambahkan Layout untuk Menu About
Buat file baru bernama about.html Isi dengan layout sederhana yang menampilkan:

Deskripsi singkat (misalnya tentang web atau pembuatnya)
Portfolio atau daftar karya/proyek
Contoh struktur:

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>About</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div id="container">
        <header>
            <h1>Tentang Saya</h1>
        </header>

        <nav>
            <a href="home.html">Home</a>
            <a href="artikel.html">Artikel</a>
            <a href="about.html" class="active">About</a>
            <a href="kontak.html">Kontak</a>
        </nav>

        <section id="main">
            <h2>Deskripsi</h2>
            <p>Halo! Saya mahasiswa Teknik Informatika di Universitas Pelita Bangsa. 
               Website ini dibuat untuk mempelajari dasar layout menggunakan HTML5 dan CSS.</p>

            <h2>Portfolio</h2>
            <ul>
                <li>Project Web Profil</li>
                <li>Aplikasi Penjualan Sederhana</li>
                <li>Desain UI Mobile</li>
            </ul>
        </section>

        <footer>
            <p>&copy; 2025 - Universitas Pelita Bangsa</p>
        </footer>
    </div>
</body>
</html>
2. Tambahkan Layout untuk Menu Contact
Buat file baru bernama kontak.html Berisi form input dengan field:

Nama
Email
Pesan
Contoh struktur:

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
            <h1>Hubungi Kami</h1>
        </header>

        <nav>
            <a href="home.html">Home</a>
            <a href="artikel.html">Artikel</a>
            <a href="about.html">About</a>
            <a href="kontak.html" class="active">Kontak</a>
        </nav>

        <section id="main">
            <h2>Formulir Kontak</h2>
            <form action="#" method="post">
                <p>
                    <label>Nama:</label><br>
                    <input type="text" name="nama" placeholder="Masukkan nama anda" required>
                </p>
                <p>
                    <label>Email:</label><br>
                    <input type="email" name="email" placeholder="Masukkan email anda" required>
                </p>
                <p>
                    <label>Pesan:</label><br>
                    <textarea name="pesan" rows="5" placeholder="Tulis pesan anda" required></textarea>
                </p>
                <p>
                    <button type="submit">Kirim</button>
                </p>
            </form>
        </section>

        <footer>
            <p>&copy; 2025 - Universitas Pelita Bangsa</p>
        </footer>
    </div>
</body>
</html>
Hasil tampilam pada browsernya:
screencapture-127-0-0-1-5500-lab4-layout1-html-2025-10-17-00_25_45
🧠 Penjelasan
Pada praktikum ini saya belajar bagaimana membuat layout web sederhana menggunakan HTML dan CSS. Langkah-langkahnya meliputi pembuatan struktur dasar halaman dengan elemen seperti header, navigasi, hero panel, main content, sidebar, dan footer. Selain itu, juga ditambahkan halaman About yang berisi deskripsi dan portfolio, serta halaman Contact yang berisi form isian nama, email, dan pesan. Semua bagian ini digabung dalam satu layout agar tampilan website menjadi lebih lengkap dan terstruktur.

✅ Kesimpulan
Melalui praktikum ini saya memahami cara menyusun layout web dengan memanfaatkan struktur HTML5 dan pengaturan CSS seperti float, margin, dan padding. Tampilan web menjadi lebih rapi, menarik, dan mudah dikembangkan untuk halaman lain. Praktikum ini juga membantu memperkuat pemahaman dasar dalam membuat desain web sederhana.
