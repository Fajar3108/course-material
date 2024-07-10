# Memulai Project dengan Go

## Membuat Project

1. Setup folder project
   ```sh
    mkdir 01-introduction-to-go
    cd 01-introduction-to-go
    go mod 01-introduction-to-go
   ```
2. Buka folder project menggunakan visual studio code
3. Buat file baru bernama main.go

   ```go
    // main.go
    package main

    import "fmt"

    func main() {
        fmt.Println("Hello World!")
    }
   ```

4. Jalankan Project
   ```sh
   go run main.go
   ```

## package main

Pada setiap project dalam golang, wajib memiliki 1 file go dengan nama package `main`. file dengan `package main` akan dieksekusi pertama kali ketika project dijalankan, bisa dibilang file dengan `package main` ini adalah entry poin/pintu masuk dari project.

Notes:
Setiap file go wajib diberikan keyword `package namapackage`, dimana biasanya namapackage sesuai dengan nama folder nya.

## Import

import digunakan untuk meng-import package lain, sehingga kita dapat menggunakan code dari package lain.

package `fmt` merupakan salah satu dari sekian banyak package bawaan yang dimiliki golang, fmt berisi banyak fungsi yang digunakan untuk keperluan input / output yang berhubungan dengan text.

Cara penggunaan keyword import

```go
// jika hanya 1 package yang perlu di import
import "nama-package"

// jika terdapat lebih dari 1 package
import (
    "package-1"
    "package-2"
)
```

## fungsi main

```go
func main() {
    // ...
}
```

`func main` adalah fungsi yang akan pertama kali dijalankan pada saat program di-eksekusi
