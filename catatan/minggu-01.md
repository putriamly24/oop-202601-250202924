# Catatan Minggu 01 : Paradigma Pemrogaman dan Setup

## Yang saya kerjakan
Saya mengerjakan tiga contoh progam Java dengan paradigma prosedural, OOP, dan fungsional. Saya juga mengisi data NIM dan nama pada file mahasiswa.properties. Setelah selesai, saya menjalankan tes menggunakan script uji.ps1 dan semua tes Minggu 1 berhasil.

## Keputusan desain
Saya menggunakan kalimat sapaan yang sama pada ketiga paradigma agar hasilnya konsisten. Pada prosedural, saya menggunakan fungsi statis . Pada OOP, saya menggunakan field private final untuk menyimpan nama danNIM. Pada fungsional, saya menggunakan lambda yang dikembalikan oleh fungsi pembuatSapaan.

## Kendala
Saya mengalami kendala saat menjalankan script karena PowerShell memblokir eksekusi file .ps1. Saya mengatasinya dengan menjalankan  script menggunakan ExecutionPolicy Bypass. Setelah itu, pengujian berhasil dengan 5 tes tanpa kegagalan.

## Penggunaan AI
- Alat yang dipakai: ChatGPT
- Bagian yang dibantu AI: Implementasi metode sapa pada HellpProsedural dan HelloOOP, serta pembuatSapaan pada HelloFungsional.
- Prompt utama: 
1. Membantu mengisi bagian TODO pada HelloProsedural.Java.
2. Membantu memperbaiki konstruktor dan metode sapa pada HelloOOP.java.
3. Membantu mengisi metode pembuatSapaan menggunakan lambda pada HelloFungsional.java
- Yang saya ubah atau tolak dari saran AI, dan alasannya: Saya menyesuaikan kode dengan struktur file yang sudah disediakan dosen dan memperbaiki kurung kurawal agar kode dapat dikomplikasi.
- Satu hal yang saya pahami lebih baik sekarang: Saya memahami perbedaan paradigma prosedural, OOP, dan fungsional serta cara menjalankan pengujian Java menggunakan Maven. 
