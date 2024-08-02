# Pengondisian

Pengondisian adalah mekanisme yang memungkinkan program untuk membuat keputusan berdasarkan kondisi tertentu. Dalam Golang, terdapat beberapa struktur kontrol yang digunakan untuk pengondisian, yaitu if, else, else if, dan switch. Mari kita bahas masing-masing struktur tersebut.

## `if` , `else if` dan `else`

Struktur if digunakan untuk menjalankan blok kode jika kondisi yang diberikan bernilai benar (true). Jika kondisi tersebut bernilai salah (false), maka blok kode di dalam if tidak akan dieksekusi.

```
if kondisi1 {
    // blok kode yang dijalankan jika kondisi1 bernilai true
} else if kondisi2 {
    // blok kode yang dijalankan jika kondisi1 bernilai false dan kondisi2 bernilai true
} else if kondisi3 {
    // blok kode yang dijalankan jika kondisi1 bernilai false dan kondisi3 bernilai true
} else {
    // blok kode yang dijalankan jika semua kondisi sebelumnya bernilai false
}
```

**Contoh:**

```go
package main

import "fmt"

func main() {
    x := 10
    if x > 10 {
        fmt.Println("x lebih besar dari 10")
    } else if x == 10 {
        fmt.Println("x sama dengan 10")
    } else {
        fmt.Println("x kurang dari 10")
    }
}
```

### Temporary Variable pada if-else

Variable Temporary adalah variable yang hanya bisa digunakan pada deret block code seleksi kondisi dimana ia ditempatkan.

```go
totalScore := 880
totalStudents := 10
if average := totalScore / total Students; average >= 90 {
    fmt.Println("Amazing!");
} else if average >= 75 {
    fmt.Println("Good!")
} else {
    fmt.Println("Need Improvement!")
}

// jika code dibawa dijalankan, akan menyebabkan error
// fmt.Println(average)
```

Variable `average` disini merupakan temporary variable, ia hanya bisa diakses pada block code `if`, `else if`, dan `else` diatas saja.

## `switch`

switch digunakan untuk memeriksa nilai dari sebuah variabel dan mencocokkannya dengan beberapa nilai yang mungkin. Ini adalah alternatif yang lebih rapi dan lebih mudah dibaca dibandingkan dengan menggunakan banyak else if.

```go
switch ekspresi {
case nilai1:
// blok kode yang dijalankan jika ekspresi == nilai1
case nilai2:
// blok kode yang dijalankan jika ekspresi == nilai2
default:
// blok kode yang dijalankan jika tidak ada case yang cocok
}
```

**Contoh:**

```go

package main

import "fmt"

func main() {
    day := "Selasa"

    switch day {
    case "Senin":
        fmt.Println("Hari ini adalah Senin")
    case "Selasa":
        fmt.Println("Hari ini adalah Selasa")
    case "Rabu":
        fmt.Println("Hari ini adalah Rabu")
    default:
        fmt.Println("Hari ini bukan Senin, Selasa, atau Rabu")
    }
}
```

### switch tanpa ekspresi

Golang juga mendukung switch tanpa ekspresi. Dalam kasus ini, setiap case harus berupa kondisi boolean.

```go
package main

import "fmt"

func main() {
    x := 7
    switch {
    case x > 10:
        fmt.Println("x lebih besar dari 10")
    case x == 7:
        fmt.Println("x sama dengan 7")
    default:
        fmt.Println("x kurang dari 10 dan tidak sama dengan 7")
    }
}
```

### Keyword `fallthrough`

Ketika fallthrough digunakan di dalam sebuah case, program akan melanjutkan eksekusi ke case berikutnya tanpa memeriksa kondisinya. fallthrough hanya dapat digunakan sebagai pernyataan terakhir dalam sebuah case dan tidak dapat diikuti oleh kode lain dalam case yang sama.

```go
package main

import "fmt"

func main() {
    day := "Senin"

    switch day {
    case "Senin":
        fmt.Println("Hari ini adalah Senin")
        fallthrough
    case "Selasa":
        fmt.Println("Hari ini adalah Selasa")
        fallthrough
    case "Rabu":
        fmt.Println("Hari ini adalah Rabu")
    default:
        fmt.Println("Hari ini bukan Senin, Selasa, atau Rabu")
    }
}
```

**Penjelasan:**

- Ketika day adalah "Senin", case "Senin" akan dieksekusi, mencetak "Hari ini adalah Senin".
- Kemudian, fallthrough akan memaksa eksekusi untuk melanjutkan ke case berikutnya, yaitu "Selasa", mencetak "Hari ini adalah Selasa".
- Karena ada fallthrough lagi, eksekusi akan berlanjut ke case "Rabu", mencetak "Hari ini adalah Rabu".

**Catatan Penting:**

- fallthrough harus digunakan dengan hati-hati karena dapat membuat program lebih sulit dipahami dan menyebabkan perilaku yang tidak diinginkan jika tidak diimplementasikan dengan benar.
- Karena fallthrough melompati pemeriksaan kondisi case berikutnya, penggunaannya bisa menyebabkan eksekusi kode yang tidak diharapkan.
- Dengan demikian, fallthrough dalam Golang memberikan fleksibilitas tambahan untuk mengelola aliran kontrol dalam pernyataan switch, tetapi harus digunakan dengan kesadaran akan dampaknya terhadap alur eksekusi program.

## Nested Condition (Pengondisian Bersarang)

Pengondisian bersarang (nested conditionals) adalah penggunaan pernyataan pengondisian seperti if, else if, else, atau switch di dalam blok pengondisian lainnya. Ini berguna ketika Anda memiliki beberapa kondisi yang perlu dievaluasi secara hierarkis atau bertingkat.

**Contoh Pengondisian Bersarang dengan `if`, `else if`, `else`**

```go
package main

import "fmt"

func main() {
    number := 5

    if number > 0 {
        fmt.Println("Angka positif")
        if number%2 == 0 {
            fmt.Println("Angka genap")
        } else {
            fmt.Println("Angka ganjil")
        }
    } else if number < 0 {
        fmt.Println("Angka negatif")
    } else {
        fmt.Println("Angka nol")
    }
}
```
