### INTEGERASI WA KE PROJECT NEXT.JS

Saya punya 2 project:

1. **Mialibels** (Next.js) - Sudah di GitHub
   Repo: https://github.com/deltanet69/Mialibels
   Ini adalah website & admin portal MI Attaqwa 15.

2. **OpenWA** (WhatsApp Gateway) - Running di localhost
   URL: http://localhost:2785
   Session ID: test-mi
   API Key: owa_k1_ba60e8764c8951dbacaa610dbbf62ab50b101ad3239d34f7bc190b6cb5ff180f

Saya perlu integrasikan OpenWA ke Mialibels untuk fitur push notifikasi tagihan SPP ke orang tua via WhatsApp.

Yang perlu dibuat:

1. Koneksi ke OpenWA API untuk kirim pesan WhatsApp
2. Fungsi ambil data tagihan siswa dari Supabase project Mi15 (students + spp_tagihan)
3. Generate template pesan tagihan SPP per siswa
4. Fungsi kirim bulk ke semua orang tua dengan delay 3-5 detik (anti-spam)
5. Fungsi kirim per siswa, dengan button action bersebalahan dengan detail tagihan
6. Simpan history pengiriman ke tabel

Data tagihan yang dibutuhkan: nama siswa, kelas, nama orang tua, nomor hp orang tua, total tagihan, total tunggakan, due date terdekat, total terbayar.


## Template Pesan WA :

Assalamu'alaikum Warahmatullahi Wabarakatuh

Kepada Yth. Bapak/Ibu [nama_orang_tua]
Orang tua dari: [nama_siswa] - Kelas [kelas]

Informasi Tagihan Keuangan MI Attaqwa 15 Babelan, untuk ananda [nama_siswa]:

{*Detail tagihan siswa sesuai dengan items yang tertunggak*}

Total Tagihan: Rp [total_tagihan]
Total Tunggakan: Rp [total_tunggakan]
Total Terbayar: Rp [total_terbayar]
Due Date Terdekat: [due_date_terdekat]

Mohon segera lakukan pembayaran untuk menghindari denda dan tunggakan lebih lanjut.

Bayar melalui transfer silahkan akses portal orang tua di :
URL : https://parent.miattaqwa15.sch.id
Login ID Siswa : [ID_SISWA]
Password : [PASSWORD]

Terima kasih


### PASTIKAN
- Hanya superadmin yang bisa akses
- Ada delay 3-5 detik antar pesan
- Responsive di mobile
- Data realtime dari Supabase

Buat kode lengkap yang siap integrasi ke project Mialibels(Mi15).

