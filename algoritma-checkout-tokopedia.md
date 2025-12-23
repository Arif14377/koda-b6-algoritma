# Algoritma Checkout Tokopedia

# Algoritma Deskriptif
1. Mulai
2. Buka website tokopedia.com
3. Cari dan Pilih produk yang akan dibeli
4. Pilih variasi produk (warna, ukuran, dll)
5. Masukkan Jumlah Barang
6. Klik tombol +Keranjang atau Beli Langsung
7. Jika belum login, maka login terlebih dahulu atau jika belum daftar, daftar terlebih dahulu.
8. Jika Tekan +Keranjang maka akan muncul pesan "Berhasil di Tambahkan" dan Tombol "Lihat Keranjang". Namun jika klik tombol "beli langsung", maka akan langsung diarahkan ke halaman Checkout (langkah ke 13).
9. Klik Lihat Keranjang, maka akan diarahkan ke keranjang
10. Ceklis produk di keranjang yang ingin dicheckout
11. Atur alamat pengiriman
12. Klik tombol "Beli" maka akan diarahkan ke halaman checkout.
13. Jika alamat belum di atur, maka tidak langsung ke halaman checkout, akan muncul pesan "Ongkir gagal ditampilkan". Atur alamat pengiriman
14. Jika sudah masuk ke halaman checkout, pilih ekspedisi jasa pengiriman
15. Pilih asuransi jika ada
16. Berikan catatan tambahan untuk penjual
17. Pilih metode pembayaran
18. Klik tombol "Bayar Sekarang"
19. Selesai

# Algoritma Flowchart
```mermaid
flowchart TD

start@{shape: circle, label: "Mulai"}
openApp@{ shape: rect, label: 'openApp: "www.tokopedia.com"'}
produk@{ shape: rect, label: "produk"}
variasiProduk@{ shape: rect, label: "variasiProduk"}
choiceProduct@{ shape: lean-r, label: '"pilih produk"'}
choiceVariasi@{ shape: lean-r, label: '"pilih variasi produk"'}
inputQty@{ shape: lean-r, label: '"masukkan jumlah barang"'}
inputProcess@{ shape: lean-r, label: 'inputKlik="+Keranjang"' }
inputProcess2@{ shape: lean-r, label: 'inputKlik="Beli langsung"' }
isLogin@{ shape: diamond, label: "isLogin?" }
loginTrue@{ shape: diamond, label: 'inputKlik == "+Keranjang"' }
loginFalse@{ shape: lean-r, label: 'Input Login: No. Telp, Password || Email, Password' }
keranjang@{ shape: rect, label: 'message: "berhasil ditambahkan"' }
keranjang2@{ shape: lean-r, label: 'Klik input: "lihat Keranjang"' }
keranjang2@{ shape: lean-r, label: 'input button: "lihat Keranjang"' }
keranjang3@{ shape: rect, label: '"List produk keranjang"' }
keranjang4@{ shape: lean-r, label: 'input: "pilih produk di keranjang"' }
keranjang5@{ shape: lean-r, label: 'input: "atur alamat pengiriman"' }
buttonBuy@{ shape: lean-r, label: 'inputButton: "Beli"' }
isAlamat@{ shape: diamond, label: 'alamat !== kosong' }
inputAlamat@{ shape: lean-r, label: "input: alamat" }
coPage@{ shape: rect, label: '"Halaman Checkout"' }
ekspedisi@{ shape: lean-r, label: 'input: "pilih ekspedisi jasa pengiriman"' }
asuransi@{ shape: lean-r, label: 'input: "pilih asuransi jika ada"' }
notes@{ shape: lean-r, label: 'input: "catatan untuk penjual"' }
payMethod@{ shape: lean-r, label: 'input: "pilih metode pembayaran"' }
buttonCheckout@{ shape: lean-r, label: 'inputButton: "Bayar sekarang"' }
stop@{shape: dbl-circ, label: "Selesai"}

isInputLogin@{ shape: diamond, label: 'email, pwd === True || phone, pwd === True' }


start-->openApp
openApp-->produk
produk-->variasiProduk
variasiProduk-->choiceProduct
choiceProduct-->choiceVariasi
choiceVariasi-->inputQty
inputQty-->inputProcess
inputQty-->inputProcess2
inputProcess-->isLogin
inputProcess2-->isLogin
isLogin--True-->loginTrue
isLogin--False-->loginFalse
loginTrue--True-->keranjang
keranjang-->keranjang2
keranjang2-->keranjang3
keranjang3-->keranjang4
keranjang4-->keranjang5
keranjang5-->buttonBuy
buttonBuy-->isAlamat
isAlamat--True-->coPage
coPage-->ekspedisi
ekspedisi-->asuransi
asuransi-->notes
notes-->payMethod
payMethod-->buttonCheckout
buttonCheckout-->stop

loginFalse-->isInputLogin
isInputLogin--True-->isLogin
loginTrue--False: Beli langsung-->isAlamat
isAlamat--False-->inputAlamat
inputAlamat-->isAlamat

```