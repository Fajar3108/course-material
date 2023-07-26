# Struktur HTML

## Anatomy of HTML Element

HTML terdiri dari beberapa elemen yang tersusun di dalam dokumen HTML. Secara anatomi, setiap elemen terdiri dari opening tag, content, dan closing tag. Di dalam opening tag terdapat atribut yang dapat diisi dengan nilai yang berbeda-beda.

![Anatomy HTML](assets/anatomy.png)

### Opening Tag

Opening tag adalah penanda pembuka dari sebuah elemen HTML. Setelahnya akan dianggap sebagai content. Penulisan opening tag menggunakan simbol < kemudian ditambah dengan tag name dan di akhiri dengan simbol >

### Closing Tag

Closing tag adalah penanda pengakhir dari sebuah elemen HTML. Setelahnya akan terdapat tag name yang sama dengan opening tag, yang membedakan adalah ditambah dengan simbol /.

### Content

Content adalah bagian dari elemen HTML yang berisi beberapa karakter atau elemen lain.
Kita juga dapat mengisi content dengan lebih dari 1 elemen yang sama atau berbeda. Kita menyebutnya dengan istilah child element.

### Element

Element (Elemen) adalah istilah 1 bagian penuh mulai dari opening tag hingga closing tag.

### Self Closing / Auto Closing Tag

HTML juga memiliki variasi tag yang tidak membutuhkan closing tag. Kita menyebutnya dengan istilah self closing tag.

Fungsinya adalah untuk mewakili beberapa elemen void atau yang tidak memerlukan sebuah content di dalamnya, seperti memunculkan gambar, menambah spasi atau menerima input.

Bentuk deklarasinya cukup sederhana, yaitu hampir sama dengan opening tag namun ditambah simbol / setelah tag name.

```html
<-- Contoh -->
<hr />
<img src="..." />
<input type="text" />
```
