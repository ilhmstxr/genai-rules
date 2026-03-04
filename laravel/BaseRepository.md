Aturan:

- Hanya berisi query (where, join, order, limit).
- Dilarang berisi logika bisnis (misal: menghitung skor kuesioner).
- Return data berupa Model atau Collection mentah.
- Untuk mencegah masalah N+1 Query, Repository harus menyediakan cara untuk melakukan Eager Loading (with()) baik melalui parameter default maupun method khusus.
- Setiap kali melakukan update() atau delete(), Service wajib menghapus cache terkait menggunakan Cache::forget($key) atau menggunakan Cache Tags jika didukung driver.
- Selalu definisikan tipe data kembalian secara eksplisit agar AI tidak memberikan nilai mixed.