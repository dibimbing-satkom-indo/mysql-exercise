# mysql-exercise
1. Aplikasi ini bisa memasukkan pesanan-pesanan makanan pelanggan
2. Aplikasi ini bisa mengeluarkan struk pembelian
3. Aplikasi ini bisa mengeluarkan laporan penghasilan mingguan dan bulanan
4. Aplikasi ini bisa mengeluarkan laporan stok

Buatlah erd dan table dengan nama database kasir_resto, 
1. API create pesanan
  - insert payment ke table payment dengan value:
    - jumlah
    - struk
    - method
    - status = 'pending'
  - insert parent pesanan ke table pesanan dengan value:
    - harga = total harga
    - jumlah = total pesanan
    - payment_id = payment.id
  - insert children pesanan ke table pesanan dengan value:
    - harga = harga di menu * jumlah
    - jumlah
    - menu_id
    - parent_pesanan_id = parent.id
  - insert struk ke table struk_pesanan dengan value:
    - meta_data
    - url
    - pesanan_id = parent.id

contoh:
1. mesen ayam bakar 2, es teh manis 1, es jeruk 1, ayam goreng 2.
