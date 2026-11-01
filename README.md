# Analisis QoS Jaringan Wi-Fi Lokal - Cintya Nur Ramdani

Pengujian Kualitas Layanan (Quality of Service) untuk koneksi ke Pico WH 192.168.4.1 menggunakan Wireshark dan CMD.

### 1. Metode Pengujian
- Ping Test 100x (ping 192.168.4.1 -n 100)
- Packet Capturing dengan Wireshark (133 detik, 3435 packets)

### 2. Rumus QoS Yang Digunakan

**a. Packet Loss:**
> Packet Loss (%) = (Paket Dikirim - Paket Diterima) / Dikirim x 100%
> = (100 - 100) / 100 x 100% = **0%**

**b. Delay / Latency:**
> Delay = Total Waktu / Jumlah Paket
> Hasil: **Average = 8 ms**

**c. Jitter:**
> Jitter = Selisih Delay Max - Min
> Hasil: **1 ms - 24 ms (StabilS)**

**d. Throughput:**
> Throughput = Total Data / Lama Pengamatan
> = 24197 Bytes / 133.803 detik = **14 kbps**

### 3. Hasil Akhir

| Parameter | Hasil | Kategori |
| :--- | :--- | :--- |
| Delay | 8 ms | Sangat Baik |
| Packet Loss | 0% | Sangat Baik |
| Jitter | Stabil | Sangat Baik |
| Throughput | 14 kbps | Baik |

> Kesimpulan: Jaringan Wi-Fi Pico WH sangat stabil dan layak untuk kontrol alat.

### 4. File Bukti
- QoS pico kel2.pcapng
- Screenshot CMD & Wireshark ada di atas
