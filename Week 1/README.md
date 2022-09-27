# Writing-and-Presentation-Test Week 1
## Day 1: Unix Command Line, Git & Github
## Unix Command Line
- Shell adalah program yang menerima perintah, kemudian meneruskan perintah tersebut ke system untuk dieksekusi.
- Command Line Interface adalah jenis shell yang berbasis teks.
- Selain command line, kita juga punya shell berbasis grafis yang lebih dikenal dengan nama GUI atau graphical user interface.
- Contoh GUI: Microsoft Windows, macOS, dan Ubuntu.
- Contoh CLI: sh, bash, zsh, cmd.exe
- Terminal Emulator adalah aplikasi untuk mengakses CLI.
#### Navigasi menggunakan CLI
- pwd (Print working directory): Command untuk melihat current working directory.
- ls (lists): Command untuk melihat isi file yang ada di sebuah direktori.
- cd <direktori> (change directory): Command untuk berpindah direktori.
#### Manipulasi file dan directory
- mkdir: Command untuk membuat direktori atau folder baru.
- mv: mencut atau memindahkan suatu file. selain itu dapat digunakan untuk merename suatu file.
- rm: menghapus suatu file.
- touch: Command untuk membuat sebuah file.
- cp: Command untuk mengcopy files atau directory
- cat: Command untuk melihat isi sebuah file.
## Git & Github
- GIT adalah Tools untuk programmer yang digunakan sebagai version control system.
- Version Control System: adalah mencatat setiap perubahan pada File (termasuk code yang kita buat) pada suatu proyek baik dikerjakan secara individu maupun tim.
- Git biasanya digunakan oleh para programmer sebagai tempat penyimpanan file pemrograman mereka, karena lebih efektif.
- File -file yg disimpan menggunakan git akan terlacak seluruh perubahannya, termasuk siapa yang mengubah.
#### Setup awal Git
- Configurasi Git: email yang disetup HARUS SAMA dengan yang digunakan pada GITHUB.
Git config –global user.name “IlyasBudi” <br />
Git config –global user.email wjati145@gmail.com
- Untuk melihat apakah setup berhasil dengan git config –list
#### Repository Git
- Repository adalah direktori proyek yang kita buat.
- Membuat repository <br />
git init (dilakukan didalam folder yang dibuat)
- git status untuk melihat apakah terjadi perubahan atau tidak pada git.
- git add untuk menambah file baru/file yang telah diubah pada git.
- git commit -m “pesan_anda” digunakan untuk menyimpan perubahan pada git.
- git log digunakan untuk melihat catatan revisi-revisi yang telah dilakukan.
- git push -u origin master digunakan untuk mengirimkan/perubahan file ke repository github.
- git branch -b [nama branch] digunakan untuk membuat branch baru.
- git checkout digunakan untuk berpindah branch.
- git revert akan membatalkan semua perubahan yang ada tanpa menghapus commit terakhir.
- jika menggunakan GIT Reset, commit terakhir akan hilang.
## Day 2:  HTML
- HTML adalah singkatan dari Hypertext Markup Language. Digunakan untuk menampilkan konten pada browser.
- Ada 2 tools utama yang harus dipersiapkan untuk membuat HTML yaitu browser dan code editor.
- Visual Studio Code merupakan salah satu code editor yang dibuat oleh Microsoft.
- Visual Studio Code merupakan paket All in One. Dapat digunakan untuk bahasa pemrograman apapun.
- Struktur HTML
```
  <!DOCTYPE html>
  <html lang="en">
    <head>
      <meta charset="UTF-8" />
      <meta http-equiv="X-UA-Compatible" content="IE=edge" />
      <meta name="viewport" content="width=device-width, initial-scale=1.0" />
      <title>Ini Judul</title>
    </head>
    <body>
      <h2>Ini Heading 1</h2>
      <h2>Ini Heading 2</h2>
      <h3>Ini Heading 3</h3>
      <article id="artikel">
        <h2>Lorem Ipsum</h2>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Libero eum porro, molestiae accusamus quaerat consectetur debitis minus illum animi recusandae aspernatur, adipisci sint accusantium officia minima facere sunt exercitationem facilis?</p>
      </article>
    </body>
  </html>
```
- HTML element terdiri atas opening tag, content, dan closing tag.<br />
  Opening tag: ``<h1>`` <br />
  Content: Ini Heading <br />
  Closing tag: ``</h1>``
- HTML Attribute adalah properties dari sebuah HTML Element. Contohnya: id, class, name.
- HTML Comment digunakan untuk memberi keterangan pada suatu line code ``<-- -->`` 
- Agar tidak perlu reload saat ada perubahan pada file HTML maka bisa menggunakan extension “Live Server” pada Visual Studio Code.
#### HTML Tag untuk menampilkan text
- Heading: yang terbesar ``<h1>`` sampai ``<h6>`` yang terkecil.
- Paragraph: ``<p>``
- Link/Anchor: ``<a>``
- List terdiri dari 2 tipe yaitu:<br />
 1. Ordered list: ``<ol>``<br />
 2. Unordered list: ``<ul>``
#### HTML Tag untuk multimedia
- Gambar: ``<img>``
- Video: ``<video>``
- Suara: ``<audio>``
#### Semantic HTML
- Semantic HTML yaitu menggunakan elemen HTML sesuai dengan kebutuhan konten. Contoh yaitu header, footer, nav, section, aside, dll.<br />
HTML4: non-semantic<br />
HTML5: Semantic
