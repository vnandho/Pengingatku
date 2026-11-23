# Pengingatku

Aplikasi Android native offline untuk alarm dan catatan melalui widget home screen. Target pengujian: Redmi Note 9 Pro, Android 12.

## Fitur
- Widget gelap glossy dengan waktu, catatan, tombol bell ON/OFF, dan panel tambah.
- Ketuk waktu untuk mengubah jam; ketuk catatan untuk mengubah catatan/detail.
- Alarm harian berulang saat aktif, dengan nada alarm perangkat dan aksi berhenti dari notifikasi.
- Data disimpan lokal di perangkat; aplikasi tidak meminta izin internet.
- Jumlah baris widget mengikuti tinggi aktual yang dilaporkan launcher, hingga 10 slot.
- Di layar aplikasi, geser baris catatan ke kiri/kanan untuk menghapus dengan animasi dan haptic feedback.
- Widget dapat diubah ukuran melalui handle resize bawaan launcher MIUI/Android.

## Memasang widget
1. Instal APK dan buka Pengingatku satu kali.
2. Tambahkan catatan dan aktifkan bell yang diperlukan.
3. Izinkan notifikasi (jika diminta) dan akses khusus **Alarms & reminders** agar alarm tepat waktu.
4. Di Home Screen, tekan lama area kosong → Widget → Pengingatku → seret ke layar.
5. Tahan widget untuk memunculkan handle resize launcher.

## Build APK dari GitHub Actions
1. Pastikan seluruh isi source project berada di root repository (folder `app/`, `build.gradle`, dan `settings.gradle`).
2. Buka tab **Actions**.
3. Jalankan workflow **Build Pengingatku APK**.
4. Setelah status sukses, buka run tersebut dan unduh artifact **Pengingatku-debug-apk**.
5. Ekstrak ZIP artifact dan instal `app-debug.apk`.

## Batasan Android widget
Widget memakai Android `RemoteViews`: interaksi langsung mendukung tap/PendingIntent, bukan gesture touch bebas. Karena itu swipe-to-delete tersedia di daftar pada layar aplikasi, bukan langsung pada widget. Resize dan getaran ketika mulai resize dikendalikan launcher MIUI/Android.

## Kompatibilitas
Redmi Note 9 Pro memiliki layar 1080 × 2400 (rasio portrait 9:20). Jumlah baris tidak dikunci berdasarkan rasio layar; aplikasi mengikuti ukuran aktual widget yang dialokasikan launcher.
