# Python - Object Oriented Programming (OOP)

Project ini berisi pembelajaran mengenai **Object Oriented Programming (OOP) pada Python**.
Materi ini membahas beberapa konsep dasar OOP seperti **Encapsulation, Inheritance, Polymorphism, dan Abstraction** serta implementasi class dan object dalam Python.

---

# Materi yang Dipelajari

Pada project ini dipelajari beberapa konsep pemrograman lanjutan Python:

1. Object Oriented Programming (OOP)
2. Modular Code
3. Efficiency Code
4. Best Practice dalam Python Coding

---

# Main Principles of OOP

## 1. Encapsulation

Encapsulation adalah teknik untuk **menyembunyikan atribut internal dari suatu class** sehingga tidak dapat diakses secara langsung dari luar class.

Atribut biasanya ditandai dengan underscore `_`.

Contoh implementasi:

```python
class User:
    def __init__(self, username, email, gender):
        self._username = username
        self._email = email
        self._gender = gender

    def get_username(self):
        return self._username

    def set_username(self, username):
        self._username = username
```

Pada contoh tersebut:

* `_username`, `_email`, dan `_gender` bersifat private
* Atribut diakses menggunakan **getter** dan **setter**

---

# 2. Inheritance

Inheritance adalah konsep **pewarisan atribut dan method dari parent class ke child class**.

Contoh:

```python
class PremiumUser(User):
    def __init__(self, username, email, gender, premium_level):
        super().__init__(username, email, gender)
        self.premium_level = premium_level
```

Class `PremiumUser` mewarisi atribut dari class `User`.

Keuntungan inheritance:

* Mengurangi pengulangan kode
* Membuat program lebih modular

---

# 3. Polymorphism

Polymorphism memungkinkan method yang sama digunakan pada **objek yang berbeda**.

Contoh implementasi:

```python
def display_user_information(user):
    user.display_user_info()
```

Fungsi tersebut dapat digunakan untuk berbagai objek yang memiliki method yang sama.

Keuntungan polymorphism:

* Kode lebih fleksibel
* Program lebih mudah dikembangkan

---

# 4. Abstraction

Abstraction digunakan untuk **menyembunyikan detail implementasi dan hanya menampilkan fungsi utama**.

Contoh menggunakan Abstract Base Class:

```python
from abc import ABC, abstractmethod

class JenisMobil(ABC):

    @abstractmethod
    def informasi(self):
        pass
```

Class turunan harus mengimplementasikan method `informasi()`.

---

# Implementasi Class dan Object

Dalam OOP, program dibangun menggunakan **class sebagai blueprint** dan **object sebagai instance dari class tersebut**.

Contoh class sederhana:

```python
class car:
    car_type = "Sedan"
    color = "Black"
```

Contoh membuat object:

```python
mobil_ayah = car()

print(mobil_ayah.car_type)
print(mobil_ayah.color)
```

---

# Constructor (**init**)

Constructor digunakan untuk **menginisialisasi atribut ketika object dibuat**.

Contoh:

```python
class Mobil:
    def __init__(self, jenis, warna):
        self.jenis_mobil = jenis
        self.warna_mobil = warna
```

---

# Contoh Program yang Dibuat

Pada bagian hands-on dibuat sebuah class **Lingkaran** untuk menghitung luas dan keliling lingkaran.

Atribut:

* radius = 10

Method:

* luas_lingkaran()
* keliling_lingkaran()

Contoh implementasi:

```python
class Lingkaran:
    def __init__(self, radius):
        self.radius = radius

    def luas_lingkaran(self):
        return 3.14 * self.radius**2

    def keliling_lingkaran(self):
        return 2 * 3.14 * self.radius
```

Contoh penggunaan:

```python
ling = Lingkaran(10)

print("Luas lingkaran:", ling.luas_lingkaran())
print("Keliling lingkaran:", ling.keliling_lingkaran())
```

Output:

```
Luas lingkaran: 314.0
Keliling lingkaran: 62.8
```

---

# Kesimpulan

Object Oriented Programming membantu membuat program yang:

* Lebih **terstruktur**
* Lebih **mudah dipahami**
* Lebih **mudah dikembangkan**

Dengan menggunakan konsep OOP seperti **Encapsulation, Inheritance, Polymorphism, dan Abstraction**, pengembangan software menjadi lebih modular dan efisien.

---

# Author

**Moh Syuril Iswan**
