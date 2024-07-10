# Operator Aritmatika

Operator aritmatika adalah operator yangd digunakan untuk melakukan operasi matematika.

| Operator |     Keterangan      |
| :------: | :-----------------: |
|   `+`    |     Penjumlahan     |
|   `-`    |     Pengurangan     |
|   `*`    |      Perkalian      |
|   `/`    |      Pembagian      |
|   `%`    | Modulus / Sisa bagi |

```go
fmt.Println(10 + 20) // 30
fmt.Println(5 - 2) // 3
fmt.Println(10 * 3) // 30
fmt.Println(6 / 2) // 3
fmt.Println(5 % 3) // 2
```

kita juga dapat mengkombinasikan beberapa operasi sekaligus

```go
fmt.Println(10 + 20 * 2) // 50
fmt.Println(5 + 2 * 3 / 3) // 7
fmt.Println((3 + 2) * 2) // 10 -> operasi didalam kurung didahulukan
```
