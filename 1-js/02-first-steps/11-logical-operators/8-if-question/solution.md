Jawabannya: pertama dan ketiga akan diexekusi.

Detil:

```js run
// Menjalankan.
// Hasil dari -1 || 0 = -1, truthy
if (-1 || 0) alert( 'first' );

// Tidak dijalankan
// -1 && 0 = 0, falsy
if (-1 && 0) alert( 'second' );

// Eksekusi
// Operator && mempunyai prioritas yang lebih tinggi daripada ||
// Jadi, -1 && 1 akan dieksekusi pertama, memberikan kita 'rantai':
// null || -1 && 1  ->  null || 1  ->  1
if (null || -1 && 1) alert( 'third' );
```

