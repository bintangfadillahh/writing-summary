# **Rangkuman Week 1**

## Unix Command Line (UCL)
- ### Shell
    Program yang digunakan untuk berkomunikasi atau memerintah sistem
- ### Command Line Interface
    Jenis shell yang berbasis teks
- ### Terminal
    Adalah aplikasi untuk mengakses CLI dimana kita dapat memberikan suatu perintah
- ### Command
    - pwd (print working directory), menampilkan current working directory
    - ls (list), command untuk melihat isi file yang ada di sebuah direktori
    - cd (change directory), command untuk berpindah direktori
    - touch, command untuk membuat file pada suatu directory
    - mkdir, command untuk membuat directory baru
    - cp (copy), untuk menyalin suatu file atau direktori
    - mv (move), untuk memindahkan suatu file atau direktori
    - rm (remove), untuk menghapus suatu file atau direktori

## Git dan Github

- ### Apa itu Git dan Github
    - Git
        Merupakan aplikasi yang digunakan untuk melacak perubahan pada folder maupun file, dan biasanya digunakan sebagai penyimpanan file program dan version control
    - Github
        Merupakan vendor penyedia layanan git berupa website penyimpanan cloud-based yang membantu menyimpan dan mengatur code, serta mengontrol perubahan pada code.

- ### Command pada Git & Github
    - git init <project-name>, membuat repositori baru
        ``` 
        git init new-project 
        ```
    - git branch -M main, untuk membuat branch baru bernama "main"
        ```
        git branch -M main
        ```
    - git add, digunakan untuk menambahkan perubahan atau file baru pada repositori untuk dilakukan commit
        ```
        git add README.txt
        ```
    - git commit -m "commit comment", untuk melakukan commit pada version control di git. 
        ```
        git commit -m "commit comment"
        ```
    - git push -u origin main, melakukan push pada repositori untuk menyimpan commit yang telah dilakukan pada repositori
        ```
        git push -u origin main
        ```
## HTML
 > HTML (Hypertext Markup Language) merupakan bahasa markup yang digunakan  untuk membuat kerangka halaman website
 - ### Struktur HTML
    ```
    <html>
    <head>
        <title>Halaman website</title>
    </head>
    <body>
        ini bagian body
    </body>
    </html>
    ```
 - ### Tag HTML
    > Tag adalah sebauh penanda awalan dan akhiran dari sebuah elemen di HTML. Tag dibuat dengan kurung siku (<...>), lalu di dalamnya berisi nama tag dan kadang berisi atribut.
  - ### Contoh Tag HTML
    - Tag untuk membuat paragraf
        ```
            <p>Ini Paragraf</p>
        ```
    - Tag untuk membuat heading
        ```
            <h1>Ini heading h1</h1>
            <h2>Ini heading h2</h2>
            <h3>Ini heading h3</h3>
            <h4>Ini heading h4</h4>
            <h5>Ini heading h5</h5>
            <h6>Ini heading h6</h6>
        ```
    - Tag untuk menambahkan image pada web
        ```
            <img src="image.png" alt="immage" />
        ```
    - Tag untuk membuat ordered/unordered list
        ```
            <ol>
                <li>list 1</li>
                <li>list 2</li>
            </ol>
            
            <ul>
                <li>list 1</li>
                <li>list 2</li>
            </ol>
        ```
    - Tag untuk membuat form
        ```
            <form>
                ....
            </form>
        ```
    - Tag untuk membuat input form
        ```
            <input type="text" name="nama" />
        ```
## CSS
> CSS adalah singkatan dari Cascading Style Sheets. CSS adalah bahasa yang digunakan untuk menambahkan design/styling ke suatu halaman website agar terlihat lebih menarik.
- ### Cara menggunakan CSS
    - Inline
        Menambahahkan CSS langsung pada element HTML
        ```
            <h1 style="color :red">Heading ini berwarna merah</p>
        ```
    - Internal
        Menambahkan tag <style> pada bagian <head>
        ```
            <head>
                <style>
                    .....
                </style>
            </head>
        ```
    - External
        Menyisipkan file .css yang terpisah dengan menggunakan tag <link> 
        ```
            <head>
                <link rel="stylesheet" href="style.css">
            </head>
        ```
- Syntax CSS
    ```
    h1 {
        color : red;
    }
    #ini_id {
        color : red;
    }
    .ini_class {
        color : red;
    }
    ```
    Keterangan
    - **h1**, **#ini_id**, dan **.ini_class** adalah sebuah selector
    - **color** adalah sebuah properti
    - **red** adalah sebuah value

## Algoritma
> Algoritma adalah proses logis yang dilakukan secara sistematis untuk menyelesaikan masalah. Basic dari permrograman adalah memecahkan suatu permasalahan, maka dari itu algoritma merupakan bagian penting dari pemrograman

- ### Penyajian Algoritma
    - **Deskriptif**, yaitu penulisan algoritma dengan cara seperti menulisa tutorial dengan bahasa sehari-hari
        ```
        Cara mengambil air minum
        1. Pergi ke dapur
        2. Ambil gelas
        3. Pergi ke dispenser
        4. Isi gelas dengan air
        ```
    - **Flow chart** atau diagram alir, penyajian algoritma yang lebih mudah dibaca karena memiliki tampilan visual berupa bagan. Flow chart menggunakan simbol bangun datar sebagai representasi dari proses yang dilakukan
    - **Pseudo Code**, penulisan algoritma ini hampir menyerupaia penulisan pada pemrograman
        ```
            Deklarasi 
                A <- "Kopi"
                B <- "Teh"
                C <- ""
            Deskripsi
                C <- A
                A <- B
                B <- C
                print(A, B)
                end
        ```
## Intro Javascript
> Javascript adalah bahasa pemrograman yang sangat powerful yang digunakan untuk logic pada sebuah website
- ### Tipe data pada javascript
    - Number
        Tipe data yang meliputi semua angka termasuk desimal
    - String
        TIpe data ini meliputi grup karakter yang ada pada keyboard kita yaitu huruf, number, spasi, simbol, dan lainnya
    - Boolean
        Tipe data yang memiliki 2 buah nilai yaitu TRUE(benar), dan FALSE(salah)
    - Null
        Null dapat diartikan sebagai sebuah variable/data yang tidak memiliki nilai 
    - Undefined
        Tipe data yang merepresentasikan variable/data yang tidak memiliki nilai karena belum didefinisikan

## Javascript Conditional dan Looping dasar
- ### Conditional
    > Condtional merupakan statement percabangan yang menggambarkan suatu kondisi
        
    - **If**
        ```
            let nilai = 10
            if(nilai == 10){
                console.log("Varible bernilai 10")
            }
        ```
    - **If else**
        ```
            let lapar = true
            if(lapar){
                console.log("Makan")
            }else{
                console.log("Tidak makan")
            }
        ```
    - **If else if**
        ```
            let stoplight = "yellow"
            if(stoplight === "red"){
                console.log("stop")
            }if else(stoplight === "yellow"){
                console.log("slow down")
            }if else(stoplight === "green"){
                console.log("go")
            }else{
                console.log("Unknown")
            }
        ```
    - **Switch case**
        ```
            let tombol = 1
            switch(tombol){
                case 1:
                    console.log("SCTV")
                    break
                case 2:
                    console.log("RCTI")
                    break
                default :
                    console.log("Channel tidak ditemukan")
            }
        ```
- ### Looping
    > looping adalah statement yang mengulang sebuah instruksi hingga kondisi terpenuhi atau jika kondisi stop/berhenti tercapai
    
    - for
        ```
            for(let i = 1; i <= 10; i++){
                console.log(i)
            }
        ```

        

