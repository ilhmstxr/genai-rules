"Saya ingin membuat Admin CRUD menggunakan Filament v3. Namun, kamu harus tetap mengintegrasikannya dengan arsitektur Service Layer saya agar logic tetap terpusat (DRY):

- Skinny Resource: Jangan menaruh logika perhitungan atau manipulasi database yang berat di dalam fungsi form() atau table() pada Filament Resource.
- Bridge to Service: Gunakan Page Hooks (seperti handleRecordCreation atau handleRecordUpdate) untuk memanggil Service yang sudah ada.
- DTO Integration: Saat melakukan aksi custom atau simpan data, ubah data array dari Filament menjadi DTO sebelum dikirim ke Service.
- Display: Untuk kolom yang membutuhkan transformasi data kompleks, Gunakan Accessors & Mutators (Attribute) di Model untuk transformasi data yang hanya bersifat display (misal: format mata uang atau penggabungan nama). Gunakan Service untuk logika yang melibatkan perhitungan database atau integrasi luar., jangan melakukan query manual di dalam skema tabel Filament.

Sekarang, tolong buatkan Filament Resource / Page untuk model  dengan detail fitur."