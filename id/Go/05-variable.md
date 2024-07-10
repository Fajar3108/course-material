# Variable

Variable berfungsi untuk menyimpan suatu nilai didalamnya, sehingga nantinya nilai tersebut dapat digunakan berulang kali (reusable).

## Deklarasi variable di Go

### 1. Menggunakan keyword `var`

```go
var name string = "fajar"
var age = 18 // boleh tanpa menuliskan tipe data
```

### 2. Menggunakan `:=` (metode type inference)

Deklarasi menggunakan tanda `:=` hanya dapat dilakukan di dalam suatu fungsi

```go
func main() {
    nilaiMtk := 90 // tidak perlu menuliskan tipe data
    var nilaiIps int8 = 80 // keyword var dapat digunakan baik di dalam maupun di luar fungsi
}
```

### 3. Multiple variable

```go
var nama, kota, jenisKelamin string = "Fajar", "Jakarta", "Laki-laki"
var usia, alamat, sudahMenikah = 30, "Kp Durian runtuh", false

func main() {
    nilaiMtk, nilaiBahasaIndo, nilaiIpa := 90, 100, 95
}
```

### 4. Reserved variable

Golang memiliki aturan unik, dimana setiap variable yang dideklarasikan tidak boleh ada yang menganggur / tidak digunakan.

tapi terkadang kita akan mendapatkan suatu nilai yang tidak kita gunakan, untuk itu go menyediakan keyword **underscore (\_)** sebgai nama dari variable yang nilainya tidak akan kita gunakan.

```go
_ = "variable sampah" // tidak perlu tanda titik dua (:)
variable1, _ := "data yang dipakai", "data tidak dipakai" // boleh pakai cara ini jika ada variable lain yang dideklrasikan bersamaan
```

## Mengubah Nilai Variable (Re-Inisialisasi)

Variable yang telah dibuat dan ditentukan nilainya, masih dapat kita ubah-ubah lagi jika diperlukan

```go
var usia int8 = 10

fmt.Println(usia) // 10

usia = 11

fmt.Println(usia) // 11
```
