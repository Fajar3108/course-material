# Operator Perbandingan

Operator perbandingan merupakan operator yang digunakan untuk membandingkan 2 buah nilai, hasil dari operator perbadningan merupakan boolean, perbandingan akan menghasilkan `true` jika benar dan `false` jika perbandingan salah.

| Operator |                           Keterangan                           |
| :------: | :------------------------------------------------------------: |
|   `==`   |         apakah nilai kiri **sama dengan** nilai kanan          |
|   `!=`   |      apakah nilai kiri **tidak sama dengan** nilai kanan       |
|   `>`    |       apakah nilai kiri **lebih besar dari** nilai kanan       |
|   `>=`   | apakah nilai kiri **lebih dari atau sama dengan** nilai kanan  |
|   `<`    |         apakah nilai kiri **kurang dari** nilai kanan          |
|   `<=`   | apakah nilai kiri **kurang dari atau sama dengan** nilai kanan |

```go
var nilai1, nilai2 int = 100, 200

fmt.Println(nilai1 == nilai2) // false
fmt.Println(nilai1 == 100) // true

fmt.Println(nilai1 != nilai2) // true
fmt.Println(nilai1 != 100) // false

fmt.Println(20 > 10) // true
fmt.Println(nilai1 > nilai2) // false

fmt.Println(nilai1 >= nilai2) // false
fmt.Println(nilai1 >= 100) // true
fmt.Println(nilai2 >= 100) // true

fmt.Println(nilai2 < 100) // false
fmt.Println(nilai1 < nilai2) // true

fmt.Println(nilai1 <= 100) // true
fmt.Println(nilai2 <= 100) // false
```
