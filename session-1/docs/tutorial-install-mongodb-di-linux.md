# Tutorial Install MogoDB di Arch Linux

## Step 1: Masuk ke Dalam Terminal
Masuk ke dalam terminal laptop atau PC yang sudah terinstal OS Arch Linux

## Step 2: Install Command `yay` di Arch Linux (jika belum terinstall)
1. `sudo pacman -Syu --needed base-devel git`

    `sudo pacman -Syu` Untuk masuk ke dalam mode `root` sekaligus memperbarui semua paket yang terinstall di sistem Arch Linux, `--needed base-devel git` untuk memastikan paket yang diperlukan untuk kompilasi `base-devel` dan `git` akan diinstall

2. `git clone https://aur.archlinux.org/yay.git`

    Command ini untuk mengunduh (kloning) *sourch code* `yay` langsung dari AUR (Arch User Repository).

3. `cd yay`

    Masuk kedalam direktori tempat *source code* `yay` diunduh, yang akan digunakan untuk kompilasi

4. `makepkg -si` 

    perintah ini mengomplikasi *source code* dan membuat paket Arch Linux. `-s` akan menginstal yang diperlukan, `-i` untuk menginstal paket yang sudah dikomplikasi

5. selesai.

## Step 3: Install Paket MongoDB 
Gunakan command `yay -S` untuk menginstall paket dari AUR (Arch User Repository), `mongodb-bin` adalah paket yang akan diinstal.

`yay -S mongodb-bin`

![mongodb](/session-1/img/tutorial%20install%20mongodb/mongodb1.jpeg)

Ketik `A` ketika ditanya "Packages to cleanBuild?"
ketik `N` ketika ditanya "Difs to show?"

![mongodb](/session-1/img/tutorial%20install%20mongodb/mongodb2.jpeg)

ketik `y` ketika ditanya "Remove make dependencis after install? 
ketik `y` ketika ditanya "Proceed with installation?" 
ketik `y` ketika ditanya "Do you want to remove these packages? 

![mongodb](/session-1/img/tutorial%20install%20mongodb/mongodb3.jpeg)

## Step 4: Jalankan Layanan MongoDB 
Setelah menginstall MongoDB, mulai layanan MongoDB dan aktifkan agar bisa berjalan saat *booting* sistem menggunakan command

`systemctl start mongodb`
`systemctl enable mongodb`

Lalu pastikan layanan berjalan dengan benar dengan menggunakan command

`systemctl status mongodb`

Output harus menunjukkan bahwa layanan dalam status *active (running)*

## Step 5: Run Mongodb
ketik `mongosh` untuk mengakses mongoDB




