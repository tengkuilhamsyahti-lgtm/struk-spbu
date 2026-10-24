# Kasir Struk SPBU

Aplikasi web untuk mencetak struk SPBU ke printer thermal 58/80 mm.

Buka lewat browser (Chrome Android atau PC), tidak perlu instal:
https://tengkuilhamsyahti-lgtm.github.io/struk-spbu/

## Fitur
- Tombol Terapkan untuk memeriksa struk dulu, baru bisa dicetak
- Bisa dipasang di HP Android (Tambahkan ke layar utama) dan tetap jalan tanpa internet
- Data usaha tersimpan otomatis di perangkat
- Edit langsung di struk (ketuk teks pratinjau), lalu kembalikan ke otomatis kapan saja
- Teks tambahan di bawah alamat, catatan transaksi, dan tulisan bawah struk bisa diubah
- Unggah logo sendiri (otomatis hitam putih untuk kertas thermal), atur lebar logo
- Atur ukuran kertas (58 mm, 80 mm, atau lebar lain), margin, dan karakter per baris
- Pengaturan printer: printer sistem atau Bluetooth, baris kosong di akhir, potong kertas, cetak uji
- Simpan dan muat cadangan pengaturan (file .json) untuk dipindah ke perangkat lain
- Isi per Rupiah atau per Liter, hitung volume, total, kembalian
- Harga BBM bisa diubah
- Nomor transaksi otomatis dan riwayat cetak ulang
- Cetak biasa atau via Bluetooth (printer thermal ESC/POS, Chrome Android)

## Jalankan di komputer sendiri
Cukup buka `index.html` di browser.

## Aplikasi Android (APK)
Unduh APK terbaru: https://github.com/tengkuilhamsyahti-lgtm/struk-spbu/releases/tag/apk-terbaru

APK dibangun otomatis oleh GitHub Actions setiap ada perubahan di folder `android/`.
APK membuka aplikasi web lewat Chrome (Trusted Web Activity), jadi cetak Bluetooth dan dialog cetak tetap berfungsi.
Perubahan tampilan cukup dilakukan di `index.html`; APK tidak perlu dibangun ulang.

### Membuka di Android Studio
1. Android Studio > File > Open, pilih folder `android/`.
2. Tunggu Gradle sync selesai, lalu Build > Build App Bundle(s) / APK(s) > Build APK(s).
3. Alamat web yang dibuka diatur di `android/app/build.gradle` (`webUrl`).

Kunci tanda tangan `android/release.jks` (sandi `strukspbu`) disimpan di repo supaya pembaruan APK bisa dipasang di atas versi lama.
Untuk rilis ke Play Store, buat kunci baru dan simpan sebagai secret, jangan di repo publik.
