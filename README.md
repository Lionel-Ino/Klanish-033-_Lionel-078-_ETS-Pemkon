# SAFE-FPID (Safety Aware and Fast Execution - Fuzzy PID)

Proyek ini adalah implementasi sistem kontrol suhu presisi menggunakan **Fuzzy-PID Controller** dengan arsitektur **Safety-Handler** yang deterministik. Sistem ini dirancang untuk berjalan pada mikrokontroler **STM32F103T6** menggunakan teknik pemrograman *bare-metal* untuk efisiensi latensi.

## Overview
SAFE-FPID memperkenalkan paradigma baru dalam kendali sensor dan aktuator dengan beralih dari pendekatan sekuensial konvensional menuju ekosistem *asynchronous* yang tangguh. Sistem ini dirancang untuk memitigasi anomali termal secara instan tanpa mengganggu stabilitas *control loop* utama.

## Fitur Utama
* **Fuzzy-PID Controller:** Algoritma kendali adaptif dengan matriks Kp yang disimpan di ROM untuk efisiensi SRAM.
* **Dual-Point Safety Handler:** Mitigasi darurat otomatis (Oven OFF, Fan 100%) jika terdeteksi selisih suhu >15°C atau suhu melampaui batas kritis 80°C.
* **Bare-Metal Optimization:** Manipulasi register tingkat rendah untuk meminimalkan latensi pembacaan ADC dan eksekusi PWM.
* **Low-Latency Telemetry:** Komunikasi data terkompresi via UART untuk visualisasi *real-time* di GNUPlot.

## Komponen Simulasi
* **Simulator:** Proteus 8 Professional.
* **IDE:** STM32CubeIDE dan Keil uVision 5.
* **Visualisasi:** GNUPlot.

## Project Structure
- `/Src`: Berisi `main.c` dengan logika SAFE-FPID.
- `/pdf`: Proposal dan evaluasi teknis.

## Author
* **Lionel Valentino Tanjung** (NRP: 2042241078)
* **Klanish Andayana Kanugraha** (NRP: 2042241033)

*Tugas Evaluasi Tengah Semester - Mata Kuliah Pemrograman Kontroler*
*Departemen Teknik Instrumentasi, ITS.*
