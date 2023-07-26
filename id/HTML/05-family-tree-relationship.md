# Family Tree Relationship

Tiap element HTML dapat saling berhubungin, kita dapat mengibaratkan seperti pohon keluarga, dimana suatu element bisa saja memiliki **parent, children, ataupun sibling**

```html
<div>
  <h1>Judul</h1>
  <p>Aku adalah sebuah paragraph</p>
  <hr />
</div>
```

## Parent Element

Parent element adalah elemen yang terhubung dan berada langsung di atas elemen lain di document tree. Dalam contoh di atas, \<div> adalah parent dari \<h1>, \<p>, dan \<hr>

## Child Element

Child element kebalikan dari parent element, yaitu elemen yang terhubung dan berada langsung di bawah elemen lain di document tree. Dalan contoh diatas \<h1>, \<p>, dan \<hr /> adalah children dari \<div>

## Sibling Element

Sibling element adalah elemen yang berbagi parent yang sama dengan elemen lain. Dalam contoh di atas, \<h1>, \<p> dan \<hr /> saling bersaudara (sibling element)
