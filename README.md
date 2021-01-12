# Nama  : Gabriel Bramafernandes
# Nim   : 19.11.2843

# Aplikasi Simulasi Pembelian Makanan Dan Minuman.
Cara kerja dan Tampilan pada aplikasi ini.

1.Tampilan Awal Pada Aplikasi.
![tampilan awal](https://user-images.githubusercontent.com/61862943/104346324-dfb6f500-5531-11eb-80a6-d7d6c522db2d.JPG)

2.Tampilan Voucher .
  Berfungsi sebagai pemilihan voucher pada aplikasi ini.
  ```
  private void generateListVoucher()
        {
            Model.Voucher awalTahun = new Model.Voucher(title: "Promo Awal Tahun Diskon 25%", discInPercent: 25);
            Model.Voucher tebusMurah = new Model.Voucher(title: "Promo Tebus Murah Diskon 30% atau max. 30.000", discInPercent: 30);
            Model.Voucher promoNatal = new Model.Voucher(title: "Promo Natal Potongan 25000", disc: 25000);

            voucherController.addItem(awalTahun);
            voucherController.addItem(tebusMurah);
            voucherController.addItem(promoNatal);

            DaftarVoucher.Items.Refresh();
        }
   ```
   Dan tampilan seperti ini.
   ![pilihan voucher](https://user-images.githubusercontent.com/61862943/104346598-31f81600-5532-11eb-8dfe-216c0a7f30f1.JPG)
 3. Tampilan Daftar Menu Yang Di Tawarkan Pada Aplikasi.
    ```
    private void generateContentPenawaran()
        {
            Item coffeLate = new Item("Coffe Late", 30000);
            Item blackTea = new Item("BlackTea", 20000);
            Item milkShake = new Item("Milk Shake", 15000);
            Item watermelonJuice = new Item("Watermelon Juice", 25000);
            Item lemonSquash = new Item("Lemon Squash", 30000);
            Item pizza = new Item("Pizza", 75000);
            Item friedRice = new Item("Fried Rice Special", 45000);

            Penawarancontroller.addItem(coffeLate);
            Penawarancontroller.addItem(blackTea);
            Penawarancontroller.addItem(milkShake);
            Penawarancontroller.addItem(watermelonJuice);
            Penawarancontroller.addItem(lemonSquash);
            Penawarancontroller.addItem(pizza);
            Penawarancontroller.addItem(friedRice);

            listPenawaran.Items.Refresh();
        }
     ```
    Ini Berfungsi Untuk Menampikan Daftar Menu Yang Akan Di Tampilkan.
    
    Dan Berikut Tampilanya ;
    ![penawaran](https://user-images.githubusercontent.com/61862943/104347097-cebab380-5532-11eb-9d1c-3774386178a6.JPG)
 4. Tampilan Setelah Memilih Beberapa Menu Yang Ingin Di Tampilkan Dan Menggunakan Salah Satu Voucher Yang Di Pilih.
 ![memilih voucher](https://user-images.githubusercontent.com/61862943/104347421-2d802d00-5533-11eb-9985-308ac6e58470.JPG)
 5. Tampilan Jika Ingin Menghapus Salah Satu Item Pada Daftar Pilihan.
    
    ```
    rivate void listBoxPesanan_ItemClicked(object sender, MouseButtonEventArgs e)
        {
            if (MessageBox.Show("Kamu ingin menghapus item ini?",
                    "Konfirmasi", MessageBoxButton.YesNo) == MessageBoxResult.Yes)
            {
                ListBox listBox = sender as ListBox;
                Item item = listBox.SelectedItem as Item;
                controller.deleteSelectedItem(item);
            }
        }
     ```
 ![tampilan jika menghapus](https://user-images.githubusercontent.com/61862943/104347647-733cf580-5533-11eb-98b4-b7543040f99b.JPG)
6. Tampilan Jika Ingin Menghapus Voucher.
    ```
  private void listBoxPakaiVoucher_ItemClicked(object sender, MouseButtonEventArgs e)
        {
            if (MessageBox.Show("Kamu ingin membatalkan voucher ini?",
                   "Konfirmasi", MessageBoxButton.YesNo) == MessageBoxResult.Yes)
            {
                ListBox listBox = sender as ListBox;
                Voucher item = listBox.SelectedItem as Voucher;
                controller.deleteSelectedVoucher(item);
            }
        }
    ```
 ![membatalkan voucher](https://user-images.githubusercontent.com/61862943/104347813-9e274980-5533-11eb-8d38-a2584ec7ecda.JPG)

   
