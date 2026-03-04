Aturan:
- Memanggil fungsi-fungsi dari Repository untuk mengambil/simpan data.
- Dilarang melakukan query database manual (selalu lewat Repository).
- Tempat melakukan validasi logika bisnis tingkat lanjut, kalkulasi skor, integrasi pihak ketiga, dan manajemen cache.
- Jika sebuah fungsi Service melakukan lebih dari satu operasi database (misal: create lalu update di tabel lain), wajib menggunakan DB::transaction()
- Gunakan throw new \Exception('Pesan error') untuk menghentikan alur jika logika bisnis tidak terpenuhi. Jangan mengembalikan pesan error sebagai return value
- Setiap kali melakukan update() atau delete(), Service wajib menghapus cache terkait menggunakan Cache::forget($key) atau menggunakan Cache Tags jika didukung driver.
- Selalu definisikan tipe data kembalian secara eksplisit agar AI tidak memberikan nilai mixed.