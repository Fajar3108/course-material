# Perulangan (Looping)

Dalam Golang, perulangan (looping) adalah mekanisme untuk mengeksekusi sekumpulan instruksi secara berulang berdasarkan kondisi tertentu. Golang hanya memiliki satu jenis perulangan yaitu for. Tidak seperti bahasa pemrograman lain yang mungkin memiliki beberapa kata kunci perulangan seperti while atau do-while, semua perulangan di Golang diimplementasikan menggunakan for.

**Struktur Dasar for**

```go
for initialization; condition; post {
    // blok kode yang dijalankan
}
```

- **Initialization**: Bagian ini dieksekusi sekali di awal sebelum perulangan dimulai. Biasanya digunakan untuk mendeklarasikan dan menginisialisasi variabel kontrol perulangan.
- **Condition**: Kondisi yang dievaluasi sebelum setiap iterasi. Jika kondisi ini bernilai benar (true), blok kode dalam perulangan akan dieksekusi. Jika bernilai salah (false), perulangan akan berhenti.
- **Post**: Ekspresi ini dieksekusi setelah setiap iterasi, biasanya digunakan untuk memperbarui variabel kontrol perulangan.

**Contoh for Sederhana**

```go
package main

import "fmt"

func main() {
    for i := 0; i < 5; i++ {
        fmt.Println("Angka:", i)
    }
}
```

**Penjelasan:**

- Initialization: i := 0 menginisialisasi variabel i dengan nilai 0.
- Condition: i < 5 memeriksa apakah i kurang dari 5. Jika benar, blok kode dijalankan.
- Post: i++ menambahkan nilai i sebanyak 1 setelah setiap iterasi.

## Perulangan Hanya Kondisi

Golang tidak memiliki kata kunci while seperti bahasa lain, tetapi kita bisa menggunakan for dengan kondisi untuk mencapai efek yang sama.

```go
package main

import "fmt"

func main() {
    count := 1
    for count <= 5 {
        fmt.Println("Count:", count)
        count++
    }
}
```

## Perulangan Tanpa Argumen

Jika hanya menyertakan for tanpa ketiga bagian (initialization, condition, dan post), ini akan menciptakan perulangan tak berhingga (infinite loop). Perulangan ini hanya akan berhenti jika ada instruksi break di dalamnya.

```go
package main

import "fmt"

func main() {
    count := 0
    for {
        fmt.Println("Infinite loop")
        count++

        // untuk mencegah infinity loop
        if count == 5 {
            break
        }
    }
}
```

## `break` dan `continue`

- break: Menghentikan perulangan dan keluar dari blok perulangan.
- continue: Melewati sisa blok kode dalam perulangan untuk iterasi saat ini dan melanjutkan ke iterasi berikutnya.

```go
package main

import "fmt"

func main() {
    for i := 0; i < 10; i++ {
        if i == 5 {
            break // menghentikan perulangan ketika i == 5
        }

        if i%2 == 0 {
            continue // melewati angka genap
        }

        fmt.Println(i)
    }
}
```

Dalam contoh ini, angka genap akan dilewati karena continue, dan perulangan akan berhenti ketika i mencapai 5 karena break.

## Nested Loop (Perulangan Bersarang)

Nested loop, atau perulangan bersarang, adalah situasi di mana satu perulangan diletakkan di dalam perulangan lainnya. Dalam Golang, nested loop dapat digunakan dengan for loops untuk mengiterasi dua atau lebih koleksi data, atau untuk melakukan operasi yang memerlukan pengulangan berlapis.

**Contoh Nested Loop Sederhana**

Misalkan kita ingin mencetak sebuah matriks 3x3:

```go
package main

import "fmt"

func main() {
    for i := 1; i <= 3; i++ {
        for j := 1; j <= 3; j++ {
            fmt.Printf("(%d, %d) ", i, j)
        }
        fmt.Println()
    }
}
```

## Looping dengan Label

Dalam Golang, label dapat digunakan dalam perulangan untuk memberikan nama tertentu pada blok kode, sehingga memungkinkan Anda untuk menggunakan pernyataan break atau continue secara lebih spesifik dan jelas, terutama dalam konteks nested loop (perulangan bersarang).

Label diidentifikasi dengan nama yang diikuti oleh titik dua (:) dan ditempatkan tepat sebelum pernyataan atau blok yang ingin diberi label. Label ini berguna untuk keluar dari loop tertentu dalam nested loop atau untuk melanjutkan iterasi dari loop tertentu, bukan hanya loop terdekat.

**Contoh Penggunaan Label**

```go
package main

import "fmt"

func main() {
    outerLoop:
    for i := 0; i < 3; i++ {
        for j := 0; j < 3; j++ {
            if i == 1 && j == 1 {
                break outerLoop // keluar dari outerLoop
            }

            fmt.Printf("(%d, %d) ", i, j)
        }

        fmt.Println()
    }

    fmt.Println("Exited from outerLoop")
}
```

Penjelasan:

- outerLoop: adalah label yang diberikan pada outer loop.
- break outerLoop: Ketika kondisi i == 1 && j == 1 terpenuhi, break ini akan keluar dari loop yang dilabeli outerLoop, menghentikan semua iterasi lebih lanjut dari loop ini dan loop yang berada di dalamnya.
