Aturan:

- Hanya berisi query (where, join, order, limit).
- Dilarang berisi logika bisnis (misal: menghitung skor kuesioner).
- Return data berupa Model atau Collection mentah.
- Untuk mencegah masalah N+1 Query, Repository harus menyediakan cara untuk melakukan Eager Loading (with()) baik melalui parameter default maupun method khusus.