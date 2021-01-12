# Nama  : Gabriel Bramafernandes
# Nim   : 19.11.2843

# Aplikasi Simulasi Pembelian Makanan Dan Minuman.
Cara kerja dan Tampilan pada aplikasi ini.

1.Tampilan Awal Pada Aplikasi.
2.Tampilan Voucher .
  Berfungsi sebagai penambhana voucher pada aplikasi ini
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
 3. 
