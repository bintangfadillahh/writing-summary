# **Rangkuman Week 2**

# **Javascript Method, Properties dan Prototype**

> Properties adalah data atau sebuah variable <br>
> Method adalah tindakan yang bisa dilakukan kepada properties, pada dasarnya adalah function

## Method string

- ### typeof

  > Digunakan untuk melakukan pengecekan type data dari suatu variabel

  ```
  let hewan = "Kucing"

  console.log(typeof hewan)
  ```

  Output :

  ```
    String
  ```

- ### length

  > length dapat mengetahui panjang atau jumlah character yang dimiliki suatu string

  ```
  let hewan = "Kucing"

  console.log(hewan.length)
  ```

  Output :

  ```
    6
  ```

- ### toUpperCase

  > Method yang digunakan untuk mengubah suatu variabel string menjadi huruf besar atau uppercase

  ```
  let hewan = "Kucing"
  console.log(hewan.toUpperCase())
  ```

  Output :

  ```
  KUCING
  ```

- ### toLowerCase

  > Method yang digunakan untuk mengubah suatu variabel string menjadi huruf kecil atau lowercase

  ```
  let hewan = "Kucing"
  console.log(hewan.toLowerCase())
  ```

  Output :

  ```
  kucing
  ```

- ### charAt

  > Method yang digunakan untuk mencari character dari string pada index tertentu

  ```
  let hewan = "Kucing"
  console.log(hewan.charAt(1))
  ```

  Output :

  ```
    U
  ```

- ### includes

  > Method ini dapat mengetahui apakah suatu variabel string memiliki character yang diinginkan dengan output berupa boolean

  ```
  let hewan = "Kucing"
  console.log(hewan.includes("c"))
  ```

  Output :

  ```
  true
  ```

- ### split

  > Method ini digunakan untuk memisahkan sebuah string menjadi data array

  ```
  let kalimat = "Kucing makan"
  console.log(kalimat.split(" "))
  ```

  Output :

  ```
  0: "Kucing"
  1: "makan"
  length: 2
  ```

## Method Number

- ### Number
  > Mengubah string yang berisi angka menjadi type data number
  ```
  Number("1234")
  ```
- ### isNaN
  > Melakukan pengecekan apakah data yang diperiksa bukan bertipe data number
  ```
  console.log(isNaN(2131)) // false
  console.log(isNaN("dawdf")) // true
  ```
- ### toFixed
  > Method yang digunakan untuk membulatkan angka desimal
  ```
  let angka = 3.12345;
  console.log(angka.toFixed(1)); // 3.1
  console.log(angka.toFixed(2)); // 3.12
  ```

## Method Math

- ### Properties
  > Property bernama Math
  ```
  console.log(Math.PI)
  ```
  Output :
  ```
  3.141592653589793
  ```
- ### Method
  ```
  console.log(Math.abs(-5)); // 5
  console.log(Math.ceil(5.2)); // 6
  console.log(Math.floor(5.6)); // 5
  console.log(Math.round(5.6)); // 6
  console.log(Math.round(5.2)); // 5
  console.log(Math.random()); // 0.123342
  ```
  > **Keterangan :** <br>
  > Math.abs mengubah angka negatif menjadi positif <br>
  > Math.ceil membulatkan angka ke atas <br>
  > Math.floor membulatkan angka ke bawah <br>
  > Math.round membuatlkan angka ke nilai terdekat <br>
  > Math.random membuat angka random <br>

## Prototype

> Prototype adalah mekanisme dalam Javascript object yang mewarasi fitur dari satu object ke object lain

- ### Membuat prototype baru

  > Kasus : membuat protype untuk menampilkan string dari index terakhir ke index pertama

  ```
  // Membuat method baru untuk data bertipe string
  String.prototype.reverse = () => {
    let s = "";
    for (let i = String(this).length - 1; i >= 0; i--) {
        s = s + String(this)[i]
    }
    return s
  }

  console.log("hallo".reverse())

  ```

  Output ;

  ```
  ollah
  ```

# DOM Intro and Traversing

> DOM (Document Object Model) adalah jembatan supaya bahasa pemrograman dapat berinteraksi dengan dokumen HTML.
> Dengan DOM, Javascript dapat memanipulasi HTML

## Traversing ke Bawah

- ### getElementBy
  - getElementById
    > Mencari element HTML dengan Id tertentu
    ```
    document.getElementById("nama-id")
    document.getElementsById("nama-id")[index] // index berupa urutan lokasi element
    ```
  - getElementByClass
    > Mencari element HTML dengan class tertentu
    ```
    document.getElementByClass("nama-class")
    ```
  - getElementByTagName
    > Mencari element HTML dengan tag tertentu
    ```
    document.getElementsByClass("ol")[0]
    ```
- ### query selector

  - querySelector

    > Akan mengambil document html pertama yang ditemukan sesuai dengan spesifikasi dan hanya akan mengambil satu

    ```
    document.querySelector(.list)
    ```

  - querySelectorAll

    > Akan mengambil document html pertama yang ditemukan sesuai dengan spesifikasi dan akan mengambil semua yang sesuai

    ```
    document.querySelectorAll(.list)
    ```

## Traversing ke Atas

> Melakukan traversing ke atas atau ke parent dari document HTML yang ditentukan

```
document.querySelector(".item").parentElement // Traversing ke parent item
document.querySelector(".item").closest(".list") // Traversing ke atas yang paling dekat
```

## Traversing ke Samping

> Traversing ke samping atau sesama child dari suatu parent

```
document.querySelector(".item").previousElementSibling // Traversing ke sibling sebelum
document.querySelector(".item").nextElementSibling // Traversing ke sibling sesudah
```

# DOM Manipulation

- ### Memberikan Content
  ```
  document.getElementById("app").innerHTML = "<p>Ini paragraf</p>"
  ```
- ### Membuat Element
  ```
  document.getElementById("app").createElement("p")
  ```
- ### Menambahkan child ke dalam parent
  ```
  document.getElementById("app").append(p)
  document.getElementById("app").appendChild(p)
  ```
- ### Menghapus element
  ```
  document.getElementById("app").remove
  ```
- ### Manipulasi atribut
  ```
  document.getElementById("link").attributes // [] list attribute
  document.getElementById("link").getAtrribut("href") // Ambil isi dari atribut href
  document.getElementById("link").setAttribut("id", "google") // Menambah atribut id dengan isi google
  ```
- ### Manipulasi style
  ```
  document.getElementById("link").style.color = "black" // Memberi warna hitam untuk font
  document.getElementById("link").style.border = "1px solid black" // Memberi border
  document.getElementById("link").removeProperty("border") // Menghapus style property border
  ```
- ### Manipulasi class
  ```
  document.getElementsByClassName("container")[0].classList // [] List dari class
  document.getElementsByClassName("container")[0].add("home") // Menambahkan class
  document.getElementsByClassName("container")[0].remove("home") // Menghapus class
  ```

# DOM Events

> Events adalah suatu kegiatan/kejadian/interaksi yang terjadi pada website

- ### Events click

  > Event click akan terjadi saat suatu document yang telah dipilih akan melakukan event saat diklik

  ```
  let paragraf = document.getElementById("paragraf")

  // cara ke-2
  paragraf.onclick = function () {
    alert("ini dari paragraf")
  }
  // paragraf.onclick = tampilkanAlert

  function tampilkanAlert () {
    alert("ini alert")
  }

  // cara ke-3
  // addEventListener bisa multiple event
  let button = document.getElementById("btn")
    button.addEventListener("click", function (event) {
    console.log(event.target)
    alert("ini dari button")
  })
  ```

- ### Membuat counter dengan events click

  ```
    let btnDecrement = document.getElementById("decrement")
    let btnIncrement = document.getElementById("increment")
    let counter = document.getElementById("counter")

    let angka = 0

    btnIncrement.addEventListener("click", function() {
        angka = angka + 1
        counter.innerText = angka
    })

    btnDecrement.addEventListener("click", function() {
        angka--
        counter.innerText = angka
    })
  ```

- ### Membuat Login

  ```
    let loginForm = document.querySelector("#sign-in")
    let inputUsername = document.querySelector('#username')
    let inputPassword = document.querySelector('#password')

    let user = {
        username: "auzan",
        password: "123"
    }

    loginForm.addEventListener("submit", (event) => {
        event.preventDefault()

        let userLogin = {
            username: inputUsername.value,
            password: inputPassword.value
        }

        console.log(userLogin);

        let login = userLogin.username == user.username &&
            userLogin.password == user.password;

        if (login) {
            console.log("selamat anda berhasil login")
        } else {
            console.log("username dan password anda salah");
        }

    // Membersihkan form
    loginForm.reset()
  ```
