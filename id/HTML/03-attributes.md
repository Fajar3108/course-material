# HTML Attributes

Pada bab sebelumnya kita telah mengetahui bagian mana yang disebut attribute. Attribute digunakan untuk memberikan informasi tambahan pada element html.

Attribute berfungsi untuk mengubah atau menyempurnakan perilaku dari elemen-elemen HTML, dan mereka didefinisikan dalam tag dengan menggunakan sintaksis tertentu.

## Global Attributes

Global Attributes adalah atribut HTML yang dapat digunakan dalam semua elemen HTML
Yang biasa dipakai yaitu attribute class & id

`id` Mengidentifikasi unik suatu elemen dalam dokumen. Biasanya digunakan untuk referensi dalam CSS atau JavaScript. value dari attribute id harus lah unik, artinya dalam 1 dokumen html tidak boleh ada element dengan id yang sama

```html
<h1 id="bab-1">Judul Bab 1</h1>
<h2 id="bab-2">Judul Bab 1</h2>
```

`class` Mirip dengan id, namun value nya dapat digunakan sebanyak yang dinginkan (tidak harus unik), dan kita dapat memberikan lebih dari 1 class untuk tiap element.

```html
<p class="paragraph">Deskripsi paragraf 1</p>
<p class="paragraph text-small">Deskripsi paragraf 2</p>
```

## Specific Tag Attributes

Beberapa elemen dalam HTML memiliki atributnya sendiri dan hanya dapat digunakan pada elemen tersebut atau beberapa elemen saja. Atribut ini adalah nilai tambahan yang akan mengkonfigurasi elemen atau menyesuaikan perilakunya untuk memenuhi kriteria yang diinginkan.

```html
<img src="put image url here" />
<input type="text" placeholder="Masukan nama anda" />
```
