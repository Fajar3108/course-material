# Tipe Data Primitive

Golang memiliki beberapa tipe data primitif yang digunakan untuk menyimpan nilai dasar. Berikut adalah tipe-tipe data primitif di Golang:

## Integer

Integer merupakan tipe data yang nilainya berupa bilangan bulat

| Tipe data | Kisaran Nilai                                         |
| :-------: | :---------------------------------------------------- |
|  `uint8`  | 0 ↔ 255                                               |
| `uint16`  | 0 ↔ 65535                                             |
| `uint32`  | 0 ↔ 4294967295                                        |
| `uint64`  | 0 ↔ 18446744073709551615                              |
|  `uint`   | sama dengan `uint32` atau `uint64` (tergantung nilai) |
|  `byte`   | sama dengan `uint8`                                   |
|  `int8`   | -128 ↔ 127                                            |
|  `int16`  | -32768 ↔ 32767                                        |
|  `int32`  | -2147483648 ↔ 2147483647                              |
|  `int64`  | -9223372036854775808 ↔ 9223372036854775807            |
|   `int`   | sama dengan `int32` atau `int64` (tergantung nilai)   |
|  `rune`   | sama dengan `int32`                                   |

## Float

Float merupakan tipe data yang nilainya berupa bilangan desimal

- `float32`: Floating point 32-bit, digunakan untuk angka desimal.
- `float64`: Floating point 64-bit, digunakan untuk angka desimal dengan presisi yang lebih tinggi.

## Boolean

Boolean hanya memiliki 2 variasi nilai, yaitu `true` dan `false`

## String

String digunakan untuk menyimpan nilai yang berupa teks. String di Go adalah urutan karakter dengan panjang tertentu dan immutable (tidak dapat diubah).

Untuk menulis nilai yang berupa string / teks, nilainya wajib diapit oleh tanda double quote atau petik 2 (")

## Contoh

```go
fmt.Println(10) // integer -> bilangan bulat
fmt.Println(2.5) // float -> bilangan desimal

// boolean
fmt.Println(true)
fmt.println(false)

// string
fmt.Println("Hello World! I am Fajar")
```
