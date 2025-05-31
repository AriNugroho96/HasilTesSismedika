## Tase Case 


### Hasil :
| TC_ID | Test Scenario | Deskripsi | Test Step | Test Data | Type | Expected Result |
|-------|---------------|-----------|-----------|-----------|------|-----------------|
| TC_01 |Berhasil Melakukan Login | Berhasil Login | 1. Bukak Halaman Login <br> 2. Input Email <br> 3. Input Password <br> 4. Klik Button "Login" | Email : arinugroho@gmailcom<br>Password : 12345678aA@ | Positif | 1.Berhasil Melakukan Login <br> 2.Setelah berhasil melakukan login masuk di halaman dashboard |
| TC_02 | Gagal Melakukan Login | Gagal Login Email tidak terdaftar | 1. Bukak Halaman Login <br> 2. Input Email <br> 3. Input Password <br> 4. Klik Button "Login" | Email :ugroho@gmail.com<br>Password : 12345678 |  Negative | 1.Gagal login di karenakan email belum terdaftar <br> 2.Menampilkan pesan error "Email tidak terdaftar" |
| TC_03 |  | Email Belum Terverifikasi | 1. Buka Halaman Login <br> 2. Input Email <br> 3. Input Password <br> 4. Klik Button "Login" | Email : nugroho@gmail.com<br>Password : 12345678aA@ | Negative | 1.Gagal login di karenakan email belum terverifikasi <br> 2.Menampilkan warning validasi "Email belum terverifikasi" |
| TC_04 |  | Email Tidak sesuai | 1. Buka Halaman Login <br> 2. Input Email <br> 3. Input Password <br> 4. Klik Button "Login" | Email : nuuuugroho@gmail.com<br>Password : 12345678aA@ | Negative | 1.Gagal login di karenakan email tidak sesuai <br> 2.Menampilkan warning validasi "Email tidak sesuai" |
| TC_05 |  | Format email tidak sesuai | 1. Buka Halaman Login <br> 2. Input Email <br> 3. Input Password <br> 4. Klik Button "Login" | Email : arinugrohoAyopmail.id<br>Password : 12345678aA@ | Negative | 1.Gagal login di karenakan format email tidak sesuai <br> 2.Menampilkan warning validasi "Format email tidak sesuai" |
| TC_06 |  | Email kosong | 1. Buka Halaman Login <br> 2. Input Email <br> 3. Input Password <br> 4. Klik Button "Login" | Email : -<br>Password : 12345678aA@ | Negative | 1.Gagal login di karenakan email kosong <br> 2.Menampilkan warning validasi "Email wajib diisi" |
| TC_07 |  | Domain Email tidak sesuai | 1. Buka Halaman Login <br> 2. Input Email <br> 3. Input Password <br> 4. Klik Button "Login" | Email : arinugroho@yopmail.id<br>Password : 12345678aA@ | Negative | 1.Gagal login di karenakan domain email tidak sesuai <br> 2.Menampilkan warning validasi "Domain email tidak sesuai" |
| TC_08 |  | Password yang di masukan salah | 1. Buka Halaman Login <br> 2. Input Email <br> 3. Input Password <br> 4. Klik Button "Login" | Email : arinugroho@gmail.com<br>Password : 111111111111 | Negative | 1.Gagal login di karenakan password yang di inputkan salah <br> 2.Menampilkan warning validasi "Password yang di inputkan salah" | 
| TC_09 |  | Password kosong | 1. Buka Halaman Login <br> 2. Input Email <br> 3. Input Password <br> 4. Klik Button "Login" | Email : arinugroho@gmail.com<br>Password : - | Negative | 1. Gagal login di karenakan password kosong <br> 2.Menampilkan warning validasi "Password wajib diisi" |
| TC_10 | Button Login | Button berhasil di klik | 1. Buka Halaman Login <br> 2. Input Email <br> 3. Input Password <br> 4. Klik Button "Login" | Klik Button "Login" | Positif | Button "login " berhasil di klik |

### Skenario Negative Testing :
| ID Skenario | Judul Skenario Pengujian | Persyaratan | Langkah- Langkah Pengujian | Data Uji | Hasil Yang Diharapkan |
|-------------|--------------------------|-------------|----------------------------|----------|-----------------------|
| NT_LOG_001 | Login dengan Username tidak terdaftar | Pengguna tidak memiliki akun terdaftar | 1. Buka halaman login. <br>2. Masukkan username yang tidak terdaftar. <br>3. Masukkan password yang valid (contoh: Password123). <br>4. Klik tombol "Login". | Username: pengguna_tidak_ada<br>Password: Password123 | Sistem menampilkan pesan kesalahan yang relevan (misalnya: "Username atau password salah." / "Akun tidak ditemukan."). Pengguna tetap di halaman login. |
| NT_LOG_002 | Login dengan Password salah | Pengguna memiliki akun terdaftar yang valid (contoh: user_valid). | 1. Buka halaman login. <br> 2. Masukkan username yang valid (contoh: user_valid). <br> 3. Masukkan password yang salah (contoh: PasswordSalah). <br> 4. Klik tombol "Login". | Username: user_valid<br>Password: PasswordSalah | Sistem menampilkan pesan kesalahan yang relevan (misalnya: "Username atau password salah." / "Kredensial tidak valid."). Pengguna tetap di halaman login. |
| NT_LOG_003 | Login dengan Username & Password kosong | Halaman login tersedia. | 1. Buka halaman login. <br> 2. Biarkan field Username kosong. <br> 3. Biarkan field Password kosong. <br> 4. Klik tombol "Login". | Username: (kosong)<br>Password: (kosong) | Sistem menampilkan pesan kesalahan yang relevan untuk setiap field kosong (misalnya: "Username tidak boleh kosong." dan "Password tidak boleh kosong.") atau pesan umum seperti "Mohon lengkapi semua field." |


### Skenario Boundary Testing Untuk Field Password:
| ID Skenario | Judul Skenario Pengujian | Persyaratan | Langkah - Langkah Pengujian | Data Uji (Password) | Hasil Yang DiHarapkan |
|-------------|--------------------------|-------------|-----------------------------|--------------------|-----------------------|
| BT_PW_001 | Verifikasi password dengan panjang kurang dari minimum | Halaman registrasi/login tersedia. | 1. Masukkan password dengan 7 karakter. <br> 2. Coba kirim formulir. | 1234567 (7 kar.) | Sistem menampilkan pesan error (misalnya: "Password harus minimal 8 karakter."). |
| BT_PW_002 | Verifikasi password dengan panjang minimum (valid) | Halaman registrasi/login tersedia. | 1. Masukkan password dengan 8 karakter. <br> 2. Coba kirim formulir. | 12345678 (8 kar.) | Sistem menerima password dan melanjutkan proses (misalnya: registrasi berhasil/login berhasil). |
| BT_PW_003 | Verifikasi password dengan panjang satu di atas minimum | Halaman registrasi/login tersedia. | 1. Masukkan password dengan 9 karakter. <br> 2. Coba kirim formulir. | 123456789 (9 kar.) | Sistem menerima password dan melanjutkan proses (misalnya: registrasi berhasil/login berhasil). |
| BT_PW_004 | Verifikasi password dengan panjang satu di bawah maksimum | Halaman registrasi/login tersedia. | 1. Masukkan password dengan 19 karakter. <br> 2. Coba kirim formulir. | P@ssw0rdPanjang19 (19 kar.) | Sistem menerima password dan melanjutkan proses. |
| BT_PW_005 | Verifikasi password dengan panjang maksimum (valid) | Halaman registrasi/login tersedia. | 1. Masukkan password dengan 20 karakter. <br> 2. Coba kirim formulir. | P@ssw0rdPanjang20! (20 kar.) | Sistem menerima password dan melanjutkan proses. |
| BT_PW_006 | Verifikasi password dengan panjang lebih dari maksimum | Halaman registrasi/login tersedia. | 1. Masukkan password dengan 21 karakter.<br>2. Coba kirim formulir. | P@ssw0rdPanjang21!! (21 kar.) | Sistem menampilkan pesan error (misalnya: "Password tidak boleh lebih dari 20 karakter.") atau memotong input secara otomatis. |

