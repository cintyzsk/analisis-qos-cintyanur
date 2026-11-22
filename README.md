# Analisis QoS Jaringan Wi-Fi Lokal - Cintya Nur Ramadani

Pengujian Kualitas Layanan (Quality of Service) untuk koneksi ke Pico WH 192.168.4.1 menggunakan Wireshark dan CMD.

## 1. Metode Pengujian
- Ping Test 100x (ping 192.168.4.1 -n 100)
- Packet Capturing dengan Wireshark (3435 packets, 133.803 detik, 241972 Bytes)
- Filter Wireshark: icmp

## 2. Rumus QoS Yang Digunakan

### a. Packet Loss:
Packet Loss (%) = (Paket Dikirim - Paket Diterima) / Dikirim x 100%
= (100 - 100) / 100 x 100% = 0%

### b. Delay / Latency:
Delay = Rata-rata Delay (dari Excel, kolom H)
= 0.019050655 detik = 19.05 ms

### c. Jitter:
Jitter = Rata-rata |Delay(n) - Delay(n-1)| (dari Excel, kolom J)
= 0.0166337 detik = 16.63 ms

### d. Throughput (Khusus Pico):
Throughput = Total Data Pico / Total Waktu Pengiriman
= 14800 Bytes / 101.994 detik = 1160.84 bps = 1.16 kbps

Throughput Total Capture Wireshark = 1808 Bytes/s = 14.47 kbps

## 3. Hasil Akhir

| Parameter | Hasil | Kategori (TIPHON) |
| --- | --- | --- |
| Delay | 19.05 ms | Sangat Baik (< 150 ms) |
| Packet Loss | 0% | Sangat Baik (< 3%) |
| Jitter | 16.63 ms | Sangat Baik (< 75 ms) |
| Throughput | 1.16 kbps | Baik (Sesuai untuk IoT / Kontrol) |

Kesimpulan: Jaringan Wi-Fi Pico WH sangat stabil, delay dan jitter rendah, tidak ada paket hilang, dan layak untuk kontrol alat berbasis IoT.

## 4. File Bukti
- QoS pico kel2.pcapng
- Screenshot CMD & Wireshark ada di atas
