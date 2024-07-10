# Introduction to Golang

Go, juga dikenal sebagai Golang, adalah bahasa pemrograman yang dikembangkan oleh Google. Go adalah bahasa pemrograman modern yang dirancang untuk efisiensi, kinerja, dan kemudahan penggunaan. Dengan dukungan yang kuat dari Google dan komunitas yang berkembang, Go menjadi pilihan populer untuk pengembangan aplikasi yang memerlukan kinerja tinggi dan kemampuan konsurensi yang baik.

## Kelebihan Go

- Sintaksis Sederhana: Go dirancang untuk memiliki sintaksis yang bersih dan mudah dipelajari.
- Kinerja Tinggi: Kompilasi ke kode mesin, menghasilkan eksekusi yang cepat.
- Konkurensi: Memiliki dukungan bawaan untuk pengelolaan konsurensi melalui goroutine dan channel, yang memudahkan penulisan program yang efisien dan paralel.
- Garbage Collection: Mengelola memori secara otomatis, sehingga programmer tidak perlu secara eksplisit mengalokasikan dan membebaskan memori.
- Statically Typed: Go adalah bahasa yang secara statis diketik, yang berarti tipe data ditentukan pada waktu kompilasi.
- Bersifat Cross-Platform: Bisa dikompilasi dan dijalankan di berbagai sistem operasi seperti Linux, macOS, dan Windows.

## Instalasi Golang

### Download Go

- Kunjungi Situs Resmi: https://golang.org/dl/
- Pilih Versi yang Tepat: Pilih versi yang sesuai dengan sistem operasi Anda (Windows, macOS, Linux).

### Windows

1. Unduh Installer: Unduh file installer .msi dari halaman unduhan Go.
2. Jalankan Installer: Klik dua kali file .msi yang telah diunduh dan ikuti petunjuk instalasi.
3. Verifikasi Instalasi:
   - Buka Command Prompt.
   - Ketik go version dan tekan Enter. Jika instalasi berhasil, Anda akan melihat versi Go yang terinstal.

### MacOS (Homebrew)

1. Pastikan homebrew telah terinstall
   jika belum, jalankan command berikut di terminal
   ```sh
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```
2. Install Go
   ```sh
   brew install go
   ```
3. Verifikasi Instalasi
   ```sh
   go version
   ```
4. Biasanya, Homebrew secara otomatis mengatur PATH Anda. Namun, jika Anda mengalami masalah dengan Go yang tidak ditemukan, Anda mungkin perlu menambahkan Go ke PATH Anda secara manual:
   ```sh
   export PATH=$PATH:/usr/local/go/bin
   source ~/.bash_profile  # atau ~/.zshrc atau ~/.profile sesuai dengan yang Anda gunakan
   ```

## Instalasi Code Editor (Visual Studio Code)

1. Download VSCode sesuai dengan OS yang kamu pakai: https://code.visualstudio.com/Download
2. Jalankan Installer: Klik dua kali file installer untuk memulai proses instalasi.
