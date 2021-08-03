# Python 3

Oleh: Deo Valiandro. M - H131 16 306

## Konsep Dasar

### Selamat datang

Python adalah salah satu bahasa pemrograman tingkat tinggi dengan aplikasi pada banyak area, mulai dari pada pemrograman web, data mining, keamanan, sampai pada mikrocontroller.

Python digunakan juga di banyak perusahaan seperti Google, NASA, CIA dan sebagainya.

> Python dijalankan menggunakan interpreter, yang artinya tidak perlu di compile untuk menjalankannya!

Pada saat tulisan ini dibuat, Python sudah mencapai versi `3.9`.

### Instalasi Python

Untuk menginstal Python, pertama-tama dengan mendownload file installernya di [website](https://www.python.org/) resmi dari Python.

Atau jika menggunakan sistem operasi Linux, maka Python sudah menjadi bawaannya. Untuk menggunakannya, dapat dengan membuka `cmd` atau `terminal`, lalu mengetikkan `python` atau `python3`.

### Program pertama

Seperti pada setiap pemrograman, hal pertama yang dilakukan adalah menjalankan ==Hello World==

Untuk menjalankan program pertama, buka terminal atau cmd, ketikkan `python`, lalu masuk kan:

```python
>>> print("Hello World")
```

Lalu, tekan <kbd>Enter</kbd>

```python
Hello World
```

Yey, berhasil...!!! :D

### Operasi sederhana

Python dapat digunakan sebagai ==kalkulator== sederhana. Coba lakukan operasi sederhana, misalnya:

```python
>>> 2 + 2
4
>>> 3 * 2 + 10
15
```

Untuk operasi aritmetika, Python menggunakan beberapa simbol:

​		<kbd>+</kbd> untuk operasi penjumlahan

​		<kbd>-</kbd> untuk operasi pengurangan

​		<kbd>/</kbd> untuk operasi pembagian

​		<kbd>*</kbd> untuk operasi perkalian

​		<kbd>//</kbd> untuk pembagian dengan pembulatan ke bawah

​		<kbd>%</kbd> untuk operasi modulo

Membagi dengan angka 0 (nol) akan dianggap error dalam Python:

```python
>>> 11 / 0
Traceback (most recent call last):
  	File "<stdin>", line 1, in <module>
ZeroDivisionError: division by zero
```

### Float/ desimal

Tipe ==data float adalah tipe data yang berisi bilangan desimal==. Misalnya:

```python
>>> 4.0 + 2.0
6.0
```

Pada Python, membagi dua int akan menghasilkan float,

```python
>>> 8 / 2
4.0
```

atau melakukan operasi aritmetika dengan 2 buah float, atau salah satunya adalah float,

```python
>>> 6 * 5.0
30.0
>>> 2.0 + 3.0
5.0
```

### Pangkat

Pada Python, pangkat dilakukan dengan menggunakan simbol <kbd>**</kbd>:

```python
>>> 2 ** 2
4
>>> 9 ** (1/2)
3.0
```

### String

Untuk ==menggunakan teks, maka kita menggunakan tipe data string==.

String dibuat dengan menggunakan tanda kutip satu (<kbd>'</kbd>), atau kutip dua (<kbd>"</kbd>). Contohnya:

```python
>>> "Hello"
'Hello'
>>> print("Hello..!!!")
Hello
```

Ada beberapa karakter yang tidak dapat langsung di ketik pada string, misalnya tanda <kbd>'</kbd> , untuk mengatasinya, digunakan tanda <kbd>\\</kbd>, contohnya:

```python
"Ini tanda petik \"."
```

contoh lain adalah tanda `\n` (_newline_) untuk membuat baris baru dan karakter <kbd>\\</kbd> (*backslash*) itu sendiri.

> Menggunakan karakter tiga petik (<kbd>"""</kbd>) pada string, akan membuat teks di print mengikuti penulisannya. Misalnya:
>
> ```python
> >>> print("""Halo,
> 		nama saya Deo""")
> Halo,
> nama saya Deo
> ```

### Input dan Output

Output pada Python menggunakan perintah `print()`. Contohnya:

```python
>>> print(2)
2
>>> print("Halo dunia")
Halo dunia
```

Input pada Python menggunakan perintah `input()`. Contohnya:

```python
>>> input("Masukkan angka sembarangan: ")
Masukkan angka sembarangan: 2
```

### Operasi pada String

Seperti pada int dan float, string juga dapat ditambah dan dikali.

> Operasi pada string disebut **concatenation**

contohnya:

```python
>>> "halo" + "dunia"
halodunia
>>> print("halo" + " " + "dunia")
halo dunia
```

walaupun ada string yang berbentuk int, lalu dijumlahkan, maka tetap akan berbentuk string, lain halnya jika int dijumlahkan dengan string, maka akan menghasilkan error.

```python
>>> "2" + "3"
23
>>> "1" + 2 + "3"
Traceback (most recent call last):
  	File "<stdin>", line 1, in <module>
TypeError: unsupported operand type(s) for +: 'int' and 'str'
```

string juga bisa di kali dengan int. Hasilnya adalah string tersebut yang di ulang-ulang. Urutan perkaliannya tidak berpengaruh, tetapi biasanya string yang ada di urutan pertama.

>  Mengalikan string dengan 0 (nol) akan menghasilkan _string_ kosong

string tidak bisa dikalikan dengan string lain dan tidak bisa juga dikalikan dengan float. Contohnya:

```python
>>> "halo"*3
halohalohalo
>> 2*"3"
33
>>> '17' * '87'
TypeError: can't multiply sequence by non-int of type 'str'
>>> "halo" * 2.0
TypeError: can't multiply sequence by non-int of type 'float'
```

### Konversi data

Untuk mengubah tipe data dari, misalnya dari string ke int, dapat dilakukan:

```python
>>> int("12") + int("3")
15
```

cara lain adalah dengan menggunakan tipe data pada input, misalnya:

```python
>>> int(input("Masukkan angka: "))
Masukkan angka: 2
```

### Variabel

==Variabel berguna untuk menyimpan nilai dengan suatu nama==. Variabel dapat digunakan berkali-kali. Misalnya:

```python
>>> x = 12
>>> print(x)
12
>>> x = 6
>>> print(x)
6
```

Penamaan variabel pada Python dapat menggunakan angka, huruf dan _underscore_. Namun, tidak dapat dimulai dengan angka. Contohnya:

```python
>>> ini_adalah_variabel = 1
>>> 123hahaha = 12
SyntaxError: invalid syntax
>>> 123 hahaha = 12
SyntaxError: invalid syntax
```

Memanggil variabel yang tidak ada akan menyebabkan error. Variabel juga dapat dihapus, caranya:

```python
>>> bar
NameError: name 'bar' is not defined
>>> foo = 12
>>> print(foo)
12
>>> del foo
>>> foo
NameError: name 'foo' is not defined
```

> Variabel foo dan bar adalah variabel **metasyntactic**, maksudnya adalah nama yang sering dijadikan alat untuk demonstrasi program

### Operator Increment

Operator increment memungkinkan kita menulis code lebih singkat, misalnya `x = x+2` menjadi `x+=2`. Hal ini juga dapat digunakan pada operasi <kbd>-</kbd>, <kbd>*</kbd>, <kbd>/</kbd>, dan <kbd>%</kbd>. Contohnya:

```python
>>> x = 2
>>> print(x)
2
>>> x += 2
>>> print(x)
4
>>> x = "b0zz"
>>> print(x)
b0zz
>>> x *= 2
>>> print(x)
b0zzb0zz
```

### Komentar

Untuk memberi komentar pada program, digunakan perintah tanda <kbd>#</kbd> pada komentar dan hanya bisa pada 1 baris, misalnya:

```python
x = 365
y = 7
# this is a comment

print(x % y) # find the remainder
# print (x // y)
# another comment
```

Hasilnya:

```python
1
```

**Docstrings** (documentation strings) adalah tanda yang mirip komentar, tetapi digunakan untuk menjelaskan kode yang ada, dan dapat lebih dari 1 baris. Contohnya:

```python
def shout(word):
    """
    Print a word with an
    exclamation mark following it.
    """
  	print(word + "!")
    
shout("spam")
```

Dan hasilnya:

```python
spam!
```

## Struktur Kontrol

### Boolean

Boolean adalah ==tipe data yang memiliki dua nilai==, yaitu `TRUE` dan `FALSE`. Boolean dapat dibuat dengan membandingkan variabel dengan menggunakan simbol:

+ <kbd>==</kbd> untuk sama dengan
+ <kbd>!=</kbd> untuk tidak sama dengan
+ <kbd>></kbd> untuk lebih besar (untuk int dan float)
+ <kbd><</kbd> untuk lebih kecil (untuk int dan float)
+ <kbd>>=</kbd> untuk lebih besar atau sama dengan (untuk int dan float)
+ <kbd><=</kbd> untuk lebih kecil atau sama dengan (untuk int dan float)

```python
>>> my_bool = True
True
>>> 1 == 2
False
>>> "foo" == "foo"
True
```

### Statemen If dan If-Else

If digunakan untuk ==melakukan perintah ketika suatu kondisi bernilai benar==. If bisa memiliki if lagi di dalamnya. Contohnya:

```python
foo = 2
if foo > 0:
	print(0)
```

Hasilnya:

```python
0
```

```python
if foo > 0:
	print(0)
	if foo > 1:
		print(1)
		if foo == 2
			print(2)
```

```python
0
1
2
```

else digunakan untuk sebagai alternatif jika kondisi if tidak terpenuhi, selain else, dapat juga digunakan multi if atau `else if` yang disingkat `elif` dalam Python. Contohnya:

```python
foo = 12
if foo/2 == 2:
	print(2)
else:
    print(4)
```

Hasilnya:

```python
4
```

Contoh lain yang menggunakan else if menggabungkan else:

```python
foo = 12
if foo/2 == 2:
	print(2)
elif foo/2 == 4:
    print(4)
elif foo/2 == 6
	print(6)
else:
    print("Tidak ada")
```

Hasilnya:

```python
6
```

### Logika Boolean

Logika boolean yaitu `and`, `or` dan `not`.

+ `and` akan bernilai benar jika kedua pernyataan benar,
+ `or` akan bernilai benar jika salah satu pernyataan benar atau keduanya benar,
+ `not` akan memberikan nilai balikan.

Contohnya:

```python
if 3 > 2 and 5 >= 4:
    print(True)
else:
    print(False)
```

Hasilnya:

```python
True
```

Contoh lainnya:

```python
>>> 1 == 1 and 2 == 2
True
>>> 1 == 1 and 2 == 3
False
>>> 1 != 1 or 2 == 2
True
>>> 2 < 1 or 3 > 6
False
>>> not 1 == 1
False
```

### Operator presedence

Di dalam Python, urutan pengerjaan suatu proses adalah sebagai berikut:

<img src="/home/deo/Documents/DownloadFile.jpeg" alt="Urutan operasi" style="zoom: 67%;" />

Contohnya:

```python
>>> False == False or True
True
>>> False == (False or True)
False
>>> (False == False) or True
True
```

### Operator while

Operator while bekerja seperti operator if, namun pada operator if hanya bisa berjalan sekali, sedangkan pada operator while, ==bisa dijalankan terus menerus selama kondisi yang diberikan terpenuhi==. Contohnya:

```python
i = 1
while i <=5:
    print(i)
   	i = i + 1

print("Finished!")
```

Hasilnya:

```python
1
2
3
4
5
Finished!
```

salah satu manfaat dari operator while adalah infinity loop,

```python
while 1==1:
  	print("In the loop")
```

> Program infinity loop dapat dihentikan dengan mengetikkan <kbd>CTRL</kbd> + <kbd>C</kbd> atau dengan menutup program

#### break

untuk ==menghentikan while tanpa mengikuti semua kemungkinan== maka digunakan `break`. Contohnya:

```python
i = 0
while 1==1:
  	print(i)
  	i = i + 1
  	if i >= 5:
    	print("Breaking")
    	break

print("Finished")
```

Hasilnya:

```python
0
1
2
3
4
Breaking
Finished
```

> Menggunakan perintah break di luar operasi perulangan seperti while akan menyebabkan error

#### continue

continue digunakan untuk ==melompati suatu while ketika terdapat kondisi tertentu==. Contohnya:

```python
i = 0
while True:
   	i = i +1
   	if i == 2:
      	print("Skipping 2")
      	continue
   	if i == 5:
      	print("Breaking")
      	break
   	print(i)

print("Finished")
```

Hasilnya:

```python
1
Skipping 2
3
4
Breaking
Finished
```

>  Menggunakan perintah continue di luar operasi perulangan seperti while akan menyebabkan error

### List

List adalah ==tipe data dalam Python yang berfungsi untuk menapung data dalam bentuk indeks==. List dibuat dengan menggunakan tanda kurung kotak (`[]`) dan setiap item dipisahkan dengan tanda koma (,).

> Indeks list dimulai dari angka 0 (nol)

Contohnya:

```python
countrys = ["Indonesia", "Malaysia", "Singapura", "Thailanf"]
print(countrys[0])
print(countrys[1])
print(countrys[2])
```

Hasilnya:

```python
Indonesia
Malaysia
Singapura
```

List kosong dapat dibuat dengan menggunakan:

```python
empty_list = []
print(empty_list)
```

Hasilnya:

```python
[]
```

List dapat menampung berbagai tipe data, misalnya int, string dan float dalam satu list.

> List dapat menampung list lainnya

Contohnya:

```python
number = 3
things = ["string", 0, [1, 2, number], 4.56]
print(things[1])
print(things[2])
print(things[2][2])
```

Hasilnya:

```python
0
[1, 2, 3]
3
```

> Membuat indeks di luar batas jumlah indeks akan menyebabkan error

Beberapa tipe data seperti string dapat dijadikan list, yang isinya adalah setiap karakter dalam string. Namun untuk int dan float, akan menyebabkan `TypeError`. Contohnya:

```python
str = "Hello world!"
print(str[6])
```

Hasilnya:

```python
w
```

### Operasi dalam list

Item di dalam indeks list dapat di ubah. Misalnya:

```python
nums = [7, 7, 7, 7, 7]
nums[2] = 5
print(nums)
```

Hasilnya:

```python
[7, 7, 5, 7, 7]
```

List  juga dapat ditambah atau dikalikan:

```python
nums = [1, 2, 3]
print(nums + [4, 5, 6])
print(nums * 3)
```

Hasilnya:

```python
[1, 2, 3, 4, 5, 6]
[1, 2, 3, 1, 2, 3, 1, 2, 3]
```

Untuk mengecek suatu item di dalam suatu list, digunakan perintah `in` dan hasilnya True jika tidak ada dan False jika tidak ada. Contohnya:

```python
foo = ["Aku", "Kamu", "Dia", "Mereka"]
print("Kamu" in foo)
print("Deo" in foo)
```

Hasilnya:

```python
True
False
```

Untuk mengecek apakah suatu item tidak ada dalam list, maka digunakan `not`. Misalnya:

```python
foo = ["Aku", "Kamu", "Dia", "Mereka"]
print("Kamu" not in foo)
print(not "Deo" in foo)
```

Hasilnya:

```python
False
True
```

Untuk menghitung jumlah indeks dalam list, digunakan perintah `len()`. Contohnya:

```pyhton
nums = [1, 3, 5, 2, 4]
print(len(nums))
```

Hasilnya:

```python
5
```

Untuk mencari indeks suatu item di dalam list, dapat digunakan `.index()`. Contohnya:

```python
letters = ['p', 'q', 'r', 's', 'p', 'u']
print(letters.index('r'))
print(letters.index('p'))
print(letters.index('z'))
```

Hasilnya:

```python
2
0
ValueError: 'z' is not in list
```

> Mencari indeks item yang tidak ada dalam list akan menyebabkan error

Untuk menambahkan item ke dalam list, maka kita dapat menggunakan perintah:

#### append

perintah `append` digunakan untuk menambahkan item ke indeks terakhir. Misalnya:

```python
nums = [1, 2, 3]
nums.append(4)
print(nums)
```

Hasilnya:

```python
[1, 2, 3, 4]
```

> append menggunakan `.` (dot) karena merupakan method

#### insert

perintah `insert` digunakan untuk menambahkan item ke indeks yang ditentukan. Misalnya:

```python
words = ["Python", "fun"]
index = 1
words.insert(index, "is")
print(words)
```

Hasilnya:

```python
['Python', 'is', 'fun']
```

### Fungsi range

Range digunakan untuk ==menyatakan angka dalam suatu batas tertentu==. Misalnya untuk membuat list dengan isi angka 0 - 9, maka kita dapat menggunakan range sebagai berikut:

```python
numbers = list(range(10))
print(numbers)
```

Maka hasilnya sebagai berikut:

```python
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```

range juga dapat menggunakan 2 parameter, yaitu parameter awal dan akhir. Misalnya:

```python
numbers = list(range(4,10))
print(numbers)
```

Hasilnya:

```python
[4, 5, 6,7, 8, 9]
```

range juga dapat menggunakan 3 parameter, di mana 2 parameter awal adalah parameter awal dan akhir sedangkan parameter ke-3 adalah interval/ lompatan.

> Parameter ketiga haruslah integer

Contohnya:

```python
numbers = list(range(5, 20, 2))
print(numbers)
```

Hasilnya:

```python
[5, 7, 9, 11, 13, 15, 17, 19]
```

### Perulangan

Perulangan adalah ==fungsi untuk melakukan sesuatu secara berulang-ulang== atau iterasi. Perulangan bisa menggunakan [while](###Operator-while) , seperti telah dijelaskan sebelumnya.

Selain while, dapat juga digunakan `for`, dengan menggunakan range.

> For mirip dengan foreach dalam bahasa pemrograman lainnya

Contohnya:

```python
words = ["hello", "world", "spam", "eggs"]
for word in words:
    print(word + "!")
```

Hasilnya:

```python
hello!
world!
spam!
eggs!
```

Contoh lainnya dengan menggunakan range:

```python
for i in range(5):
    print("hello!")
```

Hasilnya:

```python
hello!
hello!
hello!
hello!
hello!
```

## Fungsi dan Modul

### Kode yang baik

Kode yang baik adalah kode yang mudah dipahami dan gampang di ubah. Salah satu prinsip yang dikenal dalam dunia pemrograman adalah __DRY__ atau ==__Don't Repeat Yourself__==, maksudnya apa?

Maksudnya adalah untuk satu tugas tertentu, jangan tulis ulang-ulang kodenya, ==cukup sekali saja== dengan menggunakan perulangan.

> Kebalikan dari prinsip DRY adalah WET atau **Write Everything Twice**, atau **We Enjoy Typing**

### Fungsi

Fungsi adalah ==suatu struktur program yang dapat melakukan tugas tertentu secara berulang==, tergantung pada berapa banyak fungsi itu dipanggil.

Kita telah menggunakan banyak fungsi sebelumnya. Contohnya:

```python
print("Hello world!")
range(2, 20)
str(12)
range(10, 20, 3)
```

perintah `print`, `range`, `str` dan sebagainya sebenarnya adalah fungsi.

> kata di depan parameter disebut fungsi, misalnya `print`, dan isi di dalamnya adalah parameter, misalnya `hello world`.

Fungsi dapat kita definisi kan dengan menggunakan perintah `def`. Contohnya:

```python
def my_func():
    print("spam")

my_func()
```

Hasilnya:

```python
spam
```

Fungsi harus di buat sebelum dipanggil, jika tidak, maka akan menyebabkan error. Misalnya:

```python
hello()

def hello():
    print("Hello world!")
```

Hasilnya akan menyebabkan error seperti berikut:

```python
NameError: name 'hello' is not defined
```

### Fungsi dengan argumen

Fungsi bisa menerima argumen, contoh berikut adalah fungsi dengan argumen:

```python
def print_with_exclamation(word):
    print(word + "!")
    
print_with_exclamation("spam")
print_with_exclamation("eggs")
print_with_exclamation("python")
```

Hasilnya:

```python
spam!
eggs!
python!
```

Fungsi juga bisa menerima banyak argumen, misalnya:

```python
def print_sum_twice(x, y):
    print(x + y)
    print(x + y)

print_sum_twice(5, 8)
```

Hasinya:

```python
13
13
```

Argumen fungsi hanya bisa digunakan di dalam fungsi itu sendiri, jika digunakan di luar maka akan menyebabkan error, contohnya:

```python
def function(variable):
    variable += 1
    print(variable)

function(7)
print(variable)
```

Hasilnya:

```python
8
NameError: name 'variable' is not defined
```

### Mengembalikan nilai dari fungsi

Sebuah fungsi dapat mengembalikan nilai. Untuk mengembalikan nilai, digunakan perintah `return`. Contohnya:

```python
def max(x, y):
    if x >=y:
        return x
    else:
        return y
        
print(max(4, 7))
z = max(8, 5)
print(z)
```

Hasilnya:

```python
7
8
```

Sekali kita menggunakan perintah return, maka perintah dibawanya tidak akan dijalankan lagi. Misalnya:

```python
def add_numbers(x, y):
    total = x + y
    return total
	print("This won't be printed")

print(add_numbers(4, 5))
```

Hasilnya:

```python
9
```

### Fungsi sebagai objek

Fungsi dapat di _assign_ kan dengan suatu variabel maupun di _reassign_. Contohnya:

```python
def multiply(x, y):
    return x * y

a = 4
b = 7
operation = multiply
print(operation(a, b))
```

Hasilnya:

```python
28
```

Suatu fungsi juga bisa dijadikan sebagai argumen untuk fungsi lain. Misalnya:

```python
def add(x, y):
    return x + y

def do_twice(func, x, y):
    return func(func(x, y), func(x, y))

a = 5
b = 10

print(do_twice(add, a, b))
```

Hasilnya:

```python
30
```

### Modul

Modul atau module adalah ==kode yang sudah ditulis dengan tugas tertentu==, misalnya membuat angka random, operasi matematika dan fungsi lainnya.

Untuk menggunakan module, dapat digunakan perintah `import nama_modul`. Dan untuk menggunakan module yang telah dipanggil, digunakan perintah `nama_modul.variabel`. Contohnya:

```python
import random

for i in range(5):
    value = random.randint(1, 6)
    print(value)
```

Hasilnya:

```python
5
3
2
5
1
```

Jika hanya dibutuhkan fungsi tertentu dari sebuah module, maka dapat digunakan `from nama_modul import var`. Dan `var` dapat digunakan untuk melaksanakan tugas tertentu. Contohnya, misalnya untuk memanggil `pi` dari module `math`.

```python
from math import pi

print(pi)
```

Hasilnya:

```python
3.141592653589793
```

Untuk memanggil beberapa fungsi tertentu dari module, dapat menggunakan tanda koma (`,`). Misalnya:

```python
from math import pi, sqrt
```

> Menggunakan tanda aterik (*) dapat memanggil semua fungsi dari sebuah module, misalnya:
>
> ```python
> from math import *
> ```

> Mengimpor modul yang tidak ada akan menyebabkan error, misalnya:
>
> ```python
> import some_module
> ```
>
> hasilnya:
>
> ```python
> ImportError: No module named 'some_module'
> ```

Fungsi yang di import dapat di beri nama lain dari nama fungsinya, misalnya:

```python
from math import sqrt as square_root
print(square_root(100))
```

Hasilnya:

```python
10.0
```

### Library/ pustaka standar dan pip

Ada tiga jenis module di Python yaitu ==modul yang anda bisa tulis sendiri, modul yang diinstall dari sumber eksternal dan modul bawaan (pustaka standar)==.

Beberapa pustaka standar adalah: **string**, **re**, **datetime**, **math**, **random**, **os**, **multiprocessing**, **subprocess**, **socket**, **email**, **json**, **doctest**, **unittest**, **pdb**, **argparse** dan **sys**.

> Pustaka standar adalah salah satu kekuatan dari Python.

Beberapa standar pustaka ditulis dalam bahasa Python sendiri dan beberapa ditulis dalam bahasa C.

Banyak modul eksternal Python yang disimpan di **Python Package Index (PyPI)**. Untuk menggunakannya harus diinstall (membutuhkan download). Untuk menginstallnya, dapat digunakan perintah pada `cmd` dan `terminal`:

```python
pip install nama_pustaka
```

## Exception dan File

Exception adalah ==informasi yang ditampilkan ketika terdapat error pada sebuah program==. Misalnya error karena membagi bilangan dengan nol (0), atau error karena nama variabel yang dipanggil tidak ada. Contohnya:

```python
num1 = 7
num2 = 0
print(num1/num2)
```

Akan menghasilkan:

```python
ZeroDivisionError: division by zero
```

### Exception Handling

Untuk menangkap sebuah error, kita dapat menggunakan perintah `try/except`. Perintah `try` akan dijalankan dan akan langsung pindah ke perintah `except` ketika terdapat sebuah error. Jika tidak ada error, maka `except` tidak akan dijalankan. Contohnya:

```python
try:
    num1 = 7
   	num2 = 0
   	print (num1 / num2)
   	print("Done calculation")
except ZeroDivisionError:
   	print("An error occurred")
   	print("due to zero division")
```

Hasilnya:

```python
An error occurred
due to zero division
```

`try` dapat menggunakan multi `except` atau satu `except` dengan banyak parameter. Contohnya:

```python
try:
   	variable = 10
  	print(variable + "hello")
  	print(variable / 2)
except ZeroDivisionError:
   	print("Divided by zero")
except (ValueError, TypeError):
   	print("Error occurred")
```

Hasilnya:

```python
Error occurred
```

Sedangkan `try` tanpa parameter pada `except` akan menangkap semua error yang masuk ke `except`, misalnya:

```python
try:
   	word = "spam"
   	print(word / 0)
except:
   	print("An error occurred")
```

Hasilnya:

```python
An error occurred
```

### Finally

`finally` digunakan untuk menjalankan perintah tidak peduli terdapat error atau tidak. Perintah `finally` diletakkan di bawah `try/except`.

>   Kode yang ada pada `finally` akan selalu dijalankan.

Contohnya:

```python
try:
   	print("Hello")
   	print(1 / 0)
except ZeroDivisionError:
   	print("Divided by zero")
finally:
   	print("This code will run no matter what")
```

Hasilnya:

```python
Hello
Divided by zero
This code will run no matter what
```

Kode di dalam `finally` akan di jalankan terlebih dahulu walaupun terdapat error yang tidak ditangkap oleh perintah `except`. Misalnya:

```python
try:
   	print(1)
   	print(10 / 0)
except ZeroDivisionError:
   	print(unknown_var)
finally:
  	print("This is executed last")
```

Hasilnya:

```python
1
This is executed last

ZeroDivisionError: division by zero
During handling of the above exception, another exception occurred:
NameError: name 'unknown_var' is not defined
```

### Raising exception

`exception` juga bisa dimunculkan dengan menggunakan perintah `raise` namun harus jelas error yang akan dimunculkan.  Contohnya:

```python
print(1)
raise ValueError
print(2)
```

Hasilnya:

```python
1
ValueError
```

atau contoh lain:

```python
raise NameError("Invalid name!")
```

Hasilnya:

```python
NameError: Invalid name!
```

Di dalam `except`,`raise` bisa digunakan tanpa memanggil error yang dimaksud. Contohnya:

```python
try:
   	num = 5 / 0
except:
   	print("An error occurred")
   	raise
```

Hasilnya:

```python
An error occurred

ZeroDivisionError: division by zero
```

### Assertions

Assertion adalah salah satu cara mengecek error yang akan dimunculkan ketika program selesai dijalankan. Jika testing yang diberikan bernilai `false` maka akan exception-nya akan muncul. Contohnya:

```python
print(1)
assert 2 + 2 == 4
print(2)
assert 1 + 1 == 3
print(3)
```

Hasilnya:

```python
1
2
AssertionError
```

>   Assertion biasanya digunakan pada pengecekan input dan output sebuah fungsi.

Assertion juga bisa menerima parameter kedua yaitu output yang akan ditampilkan ketika error terjadi. Contohnya:

```python
temp = -10
assert (temp >= 0), "Colder than absolute zero!"
```

Hasilnya:

```python
AssertionError: Colder than absolute zero!
```

### File

Python dapat ==membuka dan mengedit file==. Namun sebelum bisa di edit, file tersebut harus dibuka terlebih dahulu.

#### membuka file

untuk membuka file, kita menggunakan perintah `open`, contohnya:

```python
myfile = open("filename.txt")
```

>   ==filename.txt== adalah nama file atau path tempat file tersebut disimpan

Untuk membuka file, juga dapat menerima argumen kedua yang mana berfungsi untuk `permision file`.

Ada beberapa kode, yaitu:

1.  `r` berfungsi untuk `read mode`,
2.  `w` untuk `write`, berarti untuk menulis ulang ke dalam file,
3.  `a` untuk `append` yaitu akan menambah sesuatu di akhir file,
4.  `b` untuk mode `binary`, digunakan untuk membuka file non-teks seperti gambar, suara, video dan berbagai format lain.

Contohnya:

```python
# write mode
open("filename.txt", "w")

# read mode
open("filename.txt", "r")
open("filename.txt")

# binary write mode
open("filename.txt", "wb")
```

>   Dapat digunakan tanda `+` untuk menambah ekstra akses, misalnya `r+` untuk mode `read` dan `write` bersamaan.

Kita dapat menampilkan isi file dengan perintah:

```python
file = open("filename.txt", "r")
cont = file.read()
print(cont)
file.close()
```

atau, kita membatasi jumlah `byte` yang dibaca,

```python
file = open("filename.txt", "r")
print(file.read(16))
print(file.read(4))
print(file.read(4))
print(file.read())
file.close()
```

>   Jika `file.read()` tidak diberikan nilai  atau negatif, maka file akan dibaca semua.

Setelah semua file di read, maka jika di read ulang, akan menghasilkan string kosong. Hal ini disebabkan program sudah mencapai `end of file`.

Untuk membaca file baris per baris, kita dapat menggunakan perintah `readline()`, contohnya jika terdapat file dengan isi:

```txt
Halo semua,
nama saya
Deo Valiandro. M
```

lalu dibaca baris per baris,

```python
file = open("filename.txt", "r")
print(file.readlines())
file.close()
```

maka akan menghasilkan:

```python
['Halo semua,\n', 'nama saya\n', 'Deo Valiandro. M']
```

dapat juga digunakan perintah `for`:

```python
file = open("filename.txt", "r")

for line in file:
    print(line)

file.close() 
```

hasilnya:

```python
Halo semua,

nama saya

Deo Valiandro. M
```

>   Di output, baris dipisahkan oleh baris kosong, karena fungsi print secara otomatis menambahkan baris baru di akhir outputnya.

#### menulis file

untuk menulis `string` ke dalam file:

```python
file = open("newfile.txt", "w")
file.write("This has been written to a file")
file.close()

file = open("newfile.txt", "r")
print(file.read())
file.close()
```

Hasilnya:

```python
This has been written to a file
```

>   Parameter `w` akan otomatis membuat file baru jika file yang dituju tidak ada

File yang sementara terbuka, isinya akan kosong. Buktinya:

```python
file = open("newfile.txt", "r")
print("Reading initial contents")
print(file.read())
print("Finished")
file.close()

file = open("newfile.txt", "w")
file.write("Some new text")
file.close()

file = open("newfile.txt", "r")
print("Reading new contents")
print(file.read())
print("Finished")
file.close()
```

Hasilnya:

```python
Reading initial contents
some initial text
Finished
Reading new contents
Some new text
Finished
```

Method `write ` akan meng-return jumlah `byte` yang ditulis ke dalam file.

```python
msg = "Hello world!"
file = open("newfile.txt", "w")
amount_written = file.write(msg)
print(amount_written)
file.close()
```

Hasilnya:

```python
12
```

>   Untuk menulis tipe data selain string, maka data tersebut harus di convert ke string.

Untuk bekerja lebih interaktif pada file, maka digunakan `try/finally`. Contohnya:

```python
try:
   	f = open("filename.txt")
   	print(f.read())
finally:
   	f.close()
```

ini akan menyebabkan file tersebut terbuka terus menerus kecuali terdapat error.

Alternatif lain adalah menggunakan perintah `with`. Contohnya:

```python
with open("filename.txt") as f:
   	print(f.read())
```

dengan cara tersebut, maka akan membuat variabel sementara (variabel `f`). File akan otomatis tertutup ketika perintah `with` selesai.

#### menutup file

setiap file yang terbuka, harus ditutup kembali setelah digunakan. Untuk melakukannya, dapat dilakukan:

```python
file = open("filename.txt", "w")
# do stuff to the file
file.close()
```

## Data Tipe Lain

### None

None adalah ==tidak adanya nilai==. None mirip dengan `null` pada pemrograman lain. None bernilai `false` ketika di konversi ke `boolean`. Contohnya:

```python
>>> None == None
True
>>> None
>>> print(None)
None
```

None juga adalah kembalian fungsi yang tidak memiliki nilai `return`:

```python
def some_func():
  	print("Hi!")

var = some_func()
print(var)
```

Hasilnya:

```python
Hi!
None
```

### Dictionary

Dictionary adalah tipe data yang berfungsi ==memasangkan suatu data dengan kunci tertentu==. Kunci yang digunakan adalah suatu integer. Dictionary ditulis dalam tanda kurung kurawal (<kbd>{}</kbd>). Dictionary dapat menampung tipe data apa saja sebagai nilai. Contohnya:

```python
ages = {"Dave": 24, "Mary": 42, "John": 58}
print(ages["Dave"])
print(ages["Mary"])
```

Hasilnya:

```python
24
42
```

>   Representasi dari setiap elemen dictionary adalah pasangan `kunci:nilai`.

Memanggil kunci yang tidak ada dalam dictionary akan menyebabkan error. Misalnya:

```python
primary = {
  	"red": [255, 0, 0], 
  	"green": [0, 255, 0], 
  	"blue": [0, 0, 255], 
}

print(primary["red"])
print(primary["yellow"])
```

Hasilnya:

```python
[255, 0, 0]

KeyError: 'yellow'
```

>   Dictionary kosong dibuat dengan menggunakan `{}`

Kunci yang digunakan haruslah objek yang immutable atau tidak dapat diubah, sehingga objek-objke mutable seperti list dan dictionary tidak dapat digunakan sebagai kunci (error jika digunakan). Contohnya:

```python
bad_dict = {
  [1, 2, 3]: "one two three", 
}
```

Hasilnya:

```python
TypeError: unhashable type: 'list'
```

Seperti list, kunci pada sebuah dictionary juga bisa di ubah nilainya. Namun tidak seperti list, pada dictionary bisa dibuat key baru dengan nilainya langsung. Misalnya:

```python
squares = {1: 1, 2: 4, 3: "error", 4: 16,}
squares[8] = 64
squares[3] = 9
print(squares)
```

Hasilnya:

```python
{1: 1, 2: 4, 3: 9, 4: 16, 8: 64}
```

Untuk mengecek sebuah kunci di dalam dictionary, dapat digunakan `in` atau `not in`. Misalnya:

```python
nums = {
    1: "one",
  	2: "two",
  	3: "three",
}
print(1 in nums)
print("three" in nums)
print(4 not in nums)
```

Hasilnya:

```python
True
False
True
```

Sebuah method yang berguna pada dictionary adalah `get` yang berguna untuk mengecek nilai seperti cara pemanggilan biasa, namun bedanya jika tidak ditemukan nilainya, maka return value-nya dapat di kustom. Contohnya:

```python
pairs = {
    1: "apple",
  	"orange": [2, 3, 4], 
  	True: False, 
  	None: "True",
}

print(pairs.get("orange"))
print(pairs.get(7))
print(pairs.get(12345, "not in dictionary"))
```

Hasilnya:

```python
[2, 3, 4]
None
not in dictionary
```

### Tuples

Tuples adalah tipe data yang mirip dengan list, ==namun bedanya tuples immutable (tidak dapat diubah)==. Tuples dibuat dengan kurung biasa, contohnya:

```python
angka = ("satu", "dua", "tiga")
```

Untuk mengaksesnya bisa dengan memanggil indeksnya:

```python
print(ankga[0])
```

Hasilnya:

```python
'satu'
```

Jika mencoba menambah data ke sebuah tuples, maka akan menyebabkan error. Misalnya:

```python
angka[3] = "empat"
```

Hasilnya:

```python
TypeError: 'tuple' object does not support item assignment
```

Tuples juga bisa dibuat tanpa kurung:

```python
my_tuple = "one", "two", "three"
print(my_tuple[0])
```

Hasilnya:

```python
one
```

atau jika ingin membuat tuple kosong:

```python
tpl = ()
```

>   Tuple lebih cepat dari list, namun nilainya tidak bisa diubah

### List Slice

Untuk menampilkan data dari list dengan lebih "advance", dapat digunakan list slice. Misalnya dengan menggunakan titik dua, `[a:b]` yang mana akan menampilkan ==data >= a dan < b (range)==. Misalnya:

```python
squares = [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
print(squares[2:6])
print(squares[3:8])
print(squares[0:1])
```

Hasilnya:

```python
[4, 9, 16, 25]
[9, 16, 25, 36, 49]
[0]
```

Jika nilai awal atau nilai akhir tidak diberikan, maka akan mengambil data dari awal tau sampai akhir. Misalnya:

```python
squares = [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
print(squares[:7])
print(squares[7:])
```

Hasilnya:

```python
[0, 1, 4, 9, 16, 25, 36]
[49, 64, 81]
```

>   `[:]` (slice) juga dapat digunakan pada tuples

Slice juga dapat menggunakan dua titik dua `[a:b:c]`, yang mana 'c' adalah nilai lompat. Misalnya:

```python
squares = [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
print(squares[::2])
print(squares[2:8:3])
```

Terlihat nilai `[2:8:3]`, berarti akan mengambil nilai mulai dari indeks 2 sampai indeks 8-1, dengan melompat-lompat setiap 3 angka, dimulai dari indeks 2, lompat 3 kali ke indeks 5.

Hasilnya:

```python
[0, 4, 16, 36, 64]
[4, 25]
```

Nilai slice yang bernilai negatif, maka nilai akan dimulai dari belakang ke depan. Contohnya:

```python
squares = [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
print(squares[1:-1])
```

Hasilnya:

```python
[1, 4, 9, 16, 25, 36, 49, 64]
```

### List Comprehensions

List dapat dibuat dengan menggunakan aturan sederhana yang diinspirasi dari notasi matematika. Misalnya menggunakan aturan for:

```python
cubes = [i**3 for i in range(5)]
print(cubes)
```

Hasilnya:

```python
[0, 1, 8, 27, 64]
```

Contoh lain dengan menggunakan if:

```python
evens=[i**2 for i in range(10) if i**2 % 2 == 0]
print(evens)
```

Hasilnya:

```python
[0, 4, 16, 36, 64]
```

Membuat list yang "terlalu besar" akan menyebabkan error ==**MemoryError**==. Misalnya:

```python
even = [2*i for i in range(10**100)]
```

akan menyebabkan error:

```python
MemoryError
```

### Format String

Cara klasik jika ingin mengkombinasikan string dan non-string adalah dengan mengconvert ke string terlebih dahulu sebelum disatukan dengan string.

Cara lain yang lebih powerfull yang bisa menggabungkan string dengan non-string adalah dengan menggunakan format string. Cara kerjanya adalah substitusi ke dalam string. Contohnya:

```python
nums = [4, 5, 6]
msg = "Numbers: {0} {1} {2}".format(nums[0], nums[1], nums[2])
print(msg)
```

Hasilnya:

```python
Numbers: 4 5 6
```

Setiap argumen yang ada di dalam tanda kurung kurawal akan diganti dengan nilai dari format string.

Selain itu, nilai pada format string juga berbentuk argumen. Contohnya:

```python
a = "{x}, {y}".format(x=5, y=12)
print(a)
```

Hasilnya:

```python
5, 12
```

### Fungsi String yang lain

Python mempunyai banyak fungsi bawaan yang berguna, misalnya:

1.  `join` &#8594; untuk menggabungkan list string
2.  `replace` &#8594; untuk mengganti string dengan string lain
3.  `startswith` dan `endswith` &#8594; untuk mengecek sub-string yang ada di awal atau akhir sebuah string
4.  `lower` dan `upper` &#8594; untuk mengubah jadi huruf kecil atau huruf besar
5.  `split` &#8594; untuk memisahkan string

Contohnya:

```python
print(", ".join(["spam", "eggs", "ham"]))
#prints "spam, eggs, ham"

print("Hello ME".replace("ME", "world"))
#prints "Hello world"

print("This is a sentence.".startswith("This"))
# prints "True"

print("This is a sentence.".endswith("sentence."))
# prints "True"

print("This is a sentence.".upper())
# prints "THIS IS A SENTENCE."

print("AN ALL CAPS SENTENCE".lower())
#prints "an all caps sentence"

print("spam, eggs, ham".split(", "))
#prints "['spam', 'eggs', 'ham']"
```

### Fungsi Numerik

Untuk fungsi yang berguna pada perhitungan numerik, 

1.  `min` &#8594; mencari nilai maksimum
2.  `max` &#8594; mencari nilai minimum
3.  `abs` &#8594; mencari nilai absolut
4.  `sum` &#8594; penjumlahan sejumlah angka

```python
print(min(1, 2, 3, 4, 0, 2, 1))
print(max([1, 4, 9, 2, 5, 6, 8]))
print(abs(-99))
print(abs(42))
print(sum([1, 2, 3, 4, 5]))
```

Hasilnya:

```python
0
9
99
42
15
```

### Fungsi List

Sebuah list dapat digunakan dalam pengkondisian dengan menggunakan `all` atau `any`. `enumerate` juga dapat digunakan untuk menampilkan list dan posisinya. Contohnya:

```python
nums = [55, 44, 33, 22, 11]

if all([i > 5 for i in nums]):
   	print("All larger than 5")

if any([i % 2 == 0 for i in nums]):
   	print("At least one is even")

for v in enumerate(nums):
   	print(v)
```

Hasilnya:

```python
All larger than 5
At least one is even
(0, 55)
(1, 44)
(2, 33)
(3, 22)
(4, 11)
```

### Analisa Teks

Misalnya kita mempunyai file txt dengan nama anu.txt:

```txt
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
```

Lalu teks dibaca:

```python
filename = input("Enter a filename: ")

with open(filename) as f:
   	text = f.read()

print(text)
```

Lalu dibuat fungsi untuk mengecek jumlah karakter yang diberikan.

```python
def count_char(text, char):
  	count = 0
  	for c in text:
    	if c == char:
      	count += 1
    return count
```

Dengan memanggil fungsi, misalnya diberikan karakter a:

```python
filename = input("Enter a filename: ")
with open(filename) as f:
  	text = f.read()

print(count_char(text, "a"))
```

Hasilnya:

```python
Enter a filename: anu.txt
22
```

Terlihat jumlah karakter 'a' adalah 22.

Dengan menambahkan perintah untuk menghitung persentase setiap karakter:

```python
for char in "abcdefghijklmnopqrstuvwxyz":
  	perc = 100 * count_char(text, char) / len(text)
  	print("{0} - {1}%".format(char, round(perc, 2)))
```

Maka akan berbentuk:

```python
def count_char(text, char):
  	count = 0
  	for c in text:
    	if c == char:
      		count += 1
  	return count

filename = input("Enter a filename: ")
with open(filename) as f:
  	text = f.read()

for char in "abcdefghijklmnopqrstuvwxyz":
  	perc = 100 * count_char(text, char) / len(text)
  	print("{0} - {1}%".format(char, round(perc, 2)))
```

Akan menghasilkan:

```python
a - 6.52%
b - 0.67%
c - 3.6%
d - 4.04%
e - 8.31%
...
...
...
z - 0.0%
```

## Pemrograman Fungsional

