Rule #1: "Selalu asumsikan saya sudah menjalankan php artisan make:arch dan file Base (BaseService/BaseRepository) sudah ada."
Rule #2: "Utamakan penggunaan Type-Hinting yang ketat (Strict Typing) sesuai standar PHP 8.2+."
Rule #3: "Jangan gunakan query builder DB::table(), selalu gunakan Eloquent melalui Repository."
Rule #4: "Wajib menggunakan Explicit Return Types pada semua method di Service dan Repository (misal: : Model, : Collection, : bool, atau : ?User). Gunakan Union Types (misal: string|int) jika diperlukan."