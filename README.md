# TP2DPBO2023

Buatlah program Java yang terkoneksi dengan database MySQL. Berikut
spesifikasi program yang harus dibuat:
- Program bebas, kecuali program Mahasiswa dan Book Author
- Terdapat proses Create, Read, Update, dan Delete data
- Terdapat proses Autentikasi (Login, Register)
- Menggunakan minimal 2 tabel pada database
- Harus terdapat minimal 1 properti gambar pada class yang dibuat (gambar akan ditampilkan pada UI)
- Terdapat pergantian screen pada UI
- Terdapat button navigasi untuk beralih screen
- List data ditampilkan menggunakan card (JPanel

## Janji
Dicki Fathurohman_2103842_Ilmu Komputer TP2 DPBO2023
Saya Dicki Fathurohman [2103842] mengerjakan TP2 DPBO2023 dalam mata kuliah DPBO, untuk keberkahanNya maka saya tidak melakukan kecurangan seperti yang telah dispesifikan. Aamiin.

## Desain

### Desain Database

Pada database, terdapat tiga tabel yang dibuat yaitu akun, artist dan album. Artist dan album memiliki relasi one to many yaitu satu artis dapat memiliki banyak album. Relasi ini dihubungkan oleh foreign key pada tabel album yaitu 'artist_id' yang tertuju ke 'id' pada tabel Artist.
![image](https://user-images.githubusercontent.com/100754802/231417156-23c33b25-e71c-4350-b2a7-48674b7d3b23.png)

### Desain Program
![image](https://user-images.githubusercontent.com/100754802/231420983-b36f4c21-0588-4e20-b245-37e1c14cafc5.png)

Terdapat 7 class yang digunakan pada program ini :
- `Class dbConnection` : Class ini berfungsi untuk menghubungkan ke database. Pada class ini terdapat dua atribut yaitu 'conn' dan 'stmt'. Metode-metode yang terdapat pada class ini digunakan untuk memproses query.
- `Class Login` : Class ini merupakan JFrame yang menampilkan form login. Pada class ini terdapat button login yang akan mengarahkan user menuju MainFrame ketika inputan username dan passwordnya sesuai.
- `Class MainFrame` : Class ini merupakan Jframe yang merupakan halaman utama untuk menampilkan data-data. Pada class ini terdapat JScrollPane yang menyimpan Card untuk ditampilkan data-datanya. Terdapat ButtonPage untuk mengganti data yang ditampilkan apakah ArtistCard atau AlbumCard. Kemudian terdapat button Add untuk menambahkan data, serta button logout untuk kembali ke halaman login.
- `Class ArtistCard` : Class ini merupakan JPanel yang digunakan untuk menampilkan data yang dimiliki tabel artist seperti name, nationality, dan foto Profile. Pada Card ini terdapat button edit untuk mengedit data dan delete untuk menghapus data.
- `Class AlbumCard` : Class ini merupakan JPanel yang digunakan untuk menampilkan data yang dimiliki tabel album seperti title, year, cover, dan artist. Pada Card ini terdapat button edit untuk mengedit data dan delete untuk menghapus data.
- `Class AddArtist` : Class ini merupakan JForm yang merupakan form untuk menambah data pada database tabel artis. Terdapat button upload untuk memilih gambar yang ingin dijadikan sebagai profile. Kemudian terdapat button submit yang berfungsi untuk melakukan AddData atau UpdateData tergantung dari atribut isUpdate.
- `Class AddAlbum` : Class ini merupakan JForm yang merupakan form untuk menambah data pada database tabel album. Terdapat button upload untuk memilih gambar yang ingin dijadikan sebagai profile. Terdapat JComboBox yang berisikan list nama artist yang ada pada database. Kemudian terdapat button submit yang berfungsi untuk melakukan AddData atau UpdateData tergantung dari atribut isUpdate.

## Alur Program
1. User mengisi username dan password pada textfield yang disediakan, kemudian menekan tombol login.
2. Jika username dan password ada pada database, maka user akan diarahkan ke MainFrame("Artist") untuk melihat daftar Artis yang ditampilkan menggunakan Card. Pada halaman ini user dapat menggunakan button dengan tulisan 'View Album Page' untuk melihat data album.
3. User dapat melakukan Logout, dan Add pada Data baik untuk artist maupun album.
4. Jika user mengklik button add pada MainFrame("Artist") maka user akan diarahkan ke AddArtist, jika pada MainFrame("Album") maka user akan diarahkan ke AddAlbum.
5. Jika user telah mengisi data menekan button submit, maka user akan diarahkan kembali ke MainFrame dan data Card pada JScrollingPane akan terupdate.
6. User dapat melakukan edit data dengan mengklik button edit pada Card.
7. User dapat melakukan delete data dengan mengklik button delete pada Card. Jika user menghapus data artist, maka data album dengan foreign key yg merujuk ke artist tersebut akan ikut terhapus.

`Akun`
- username : dicki
- password : dicki

## Dokumentasi

![image](https://user-images.githubusercontent.com/100754802/231428246-15e012a0-c27c-4029-9287-c1e4da44e5a8.png)
![image](https://user-images.githubusercontent.com/100754802/231428404-e73bfe1e-9ecf-4efd-93b1-d738f663e95f.png)
![image](https://user-images.githubusercontent.com/100754802/231428466-1f76d337-1e8b-4dec-a832-f9da0e0eeb23.png)
![image](https://user-images.githubusercontent.com/100754802/231428625-10296bf6-4902-48fc-a7a1-96f50ce95786.png)
![image](https://user-images.githubusercontent.com/100754802/231428763-4189a871-7351-47d2-811c-2d76cf655266.png)
![image](https://user-images.githubusercontent.com/100754802/231428811-56cb73a0-688b-4271-a487-51cb39cabebd.png)
![image](https://user-images.githubusercontent.com/100754802/231428898-e2a24756-7d5e-4bd4-9bb7-2a7619ee069d.png)






