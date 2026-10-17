# FlyWare

Proyek ini adalah bot Minecraft (berbasis Mineflayer) yang dikendalikan oleh simulasi jaringan saraf *Leaky Integrate-and-Fire* (LIF). Sistem ini mensimulasikan "otak" lalat buah (*Drosophila melanogaster*) untuk memproses input sensorik dari lingkungan Minecraft dan menghasilkan output motorik untuk bernavigasi dan menghindari rintangan.

## Fitur Utama

* **Integrasi Mineflayer**: Bot dapat bergabung ke server Minecraft, membaca kondisi sekitar (rintangan, level cahaya, pemain lain), dan bergerak secara otonom.
* **Simulasi Saraf LIF**: Menggunakan model matematika *Leaky Integrate-and-Fire* untuk mensimulasikan lonjakan tegangan (*spike*) pada neuron, persis seperti cara kerja saraf biologis.
* **Dua Mode Eksekusi**: 
  * **Demo Mode**: Menggunakan konektom sintetis yang dibuat secara prosedural untuk pengujian cepat.
  * **Hemibrain Mode**: Menarik data sirkuit saraf asli (konektom navigasi) dari Janelia FlyWire API (neuPrint) untuk pengujian biologis yang lebih akurat.

## Persyaratan Sistem

* Node.js (v16 atau lebih baru)
* Python 3.x (hanya diperlukan untuk mode Hemibrain)
* Server Minecraft lokal (disarankan menjalankan Paper/Spigot di `localhost:25565` dengan *offline mode* aktif untuk pengujian)

## Instalasi

1. Kloning repositori ini:
   ```bash
   git clone [https://github.com/username-kamu/nama-repo.git](https://github.com/username-kamu/nama-repo.git)
   cd nama-repo

## How To Run
1. Hasilkan data Konektomversi demo dengan menjalankan perintah
   npm run gen-demo-data
2. Mulai menguji coba bot dengan perintah
   npm start


## Apabila ingin menggunakan versi data otak asli dari lalat

Mode ini menggunakan data konektom navigasi lalat asli (seperti neuron sensorik, kompas navigasi EPG, dan neuron motorik DNa/DNb).

1. Instal *library* Python pendukung:
   ```bash
   pip install neuprint-python
2. Dapatkaan token dari website neuJaneila
   lalu masukkan disini
    ```bash
    set NEUPRINT_TOKEN="xxx"
3. Lakukan penarikan data dari otak API key dengan perintah
    ```bash
    python scripts/fetch_hemibrain.py
4. Lalu jalankan bot dengan perintah
    ```bash
    npm start
