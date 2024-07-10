# Konstanta

Konstanta seperti namanya yaitu nilai yang bersifat tetap. Konstanta adalah variable dimana nilainya tidak dapat diubah lagi setelah dideklarasikan. Inisialisasi nilai konstanta hanya bisa dilakukan diawal bersamaan dengan saat deklarasi.

## Deklarasi Variable Konstanta

Cara deklarasi variable konstanta sama saja dengan variable biasanya, hanya saja keyword `var` diganti dengan keyword `const`.

```go
const pi float32 = 3.14
const myGender string = "male"
```

## Deklarasi Multi Konstanta

```go
const (
    pi float32 = 3.14
    myGender string = "male"
    totalMonths = 12
)
```
