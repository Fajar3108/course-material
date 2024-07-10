# Operator Logika

Operator logika digunakan dalam Golang untuk melakukan operasi logika pada nilai boolean. Berikut adalah operator logika yang tersedia di Golang beserta contoh penggunaannya:

|         Operator          | Keterangan |
| :-----------------------: | :--------: |
|           `&&`            |    AND     |
| <code>&#124;&#124;</code> |     OR     |
|            `!`            |    NOT     |

## AND (&&)

Jika kedua nilainya `true` maka akan menghasilkan `true`, namun jika salah satu nilainya saja adalah `false` maka akan menghasilkan `false`.

```go
fmt.Println(true && true) // true
fmt.Println(true && false) // false
fmt.Println(false && false) // false
```

## OR (`||`)

Jika salah satunya saja bernilai `true` maka akan menghasilkan `true`.

```go
fmt.Println(true && true) // true
fmt.Println(true && false) // true
fmt.Println(false && false) // false
```

## Not (`!`)

Operator Not `!` juga dapat digunakan untuk membalikan nilai boolean, jadi nilai `true` jika diberi operator not akan menghasilkan false

```go
fmt.Println(!true) // false
fmt.Println(!false) // true
```
