# Caj Payment Gateway Malaysia (FPX, kad, DuitNow QR): data terbuka

Perbandingan caj **FPX, kad dan DuitNow QR** bagi payment gateway popular di Malaysia, dalam format **JSON dan CSV**. Kadar dibaca terus dari laman harga rasmi setiap gateway pada **17 November 2026**.

**Nak kira caj untuk bisnes anda?** Guna [Kalkulator Caj FPX](https://miraclemikhael.com/ms/alat/kalkulator-caj-fpx) (percuma, Bahasa Melayu): masukkan jumlah bayaran dan bilangan transaksi sebulan, dan ia susun gateway dari yang paling murah.

## Caj untuk satu bayaran (RM)
| Gateway | FPX RM50 | FPX RM500 | FPX B2B RM5,000 | Kad RM100 | DuitNow QR RM50 | Yuran tahunan |
| --- | --- | --- | --- | --- | --- | --- |
| [Billplz Basic](https://main.billplz.com/pricing) | RM1.25 | RM1.25 | RM3.00 | RM1.80 | RM0.75 | 0 |
| [Billplz Standard](https://main.billplz.com/pricing) | RM0.75 | RM0.75 | RM2.00 | RM1.50 | RM0.75 | RM999 |
| [toyyibPay Standard](https://www.toyyibpay.com/pricing-plans/) | RM1.00 | RM1.00 | RM2.00 | RM1.50 | RM0.50 | 0 |
| [CHIP](https://www.chip-in.asia/pricing) | RM1.08 | RM1.08 | RM2.16 | RM2.16 | RM0.54 | 0 |
| [HitPay](https://hitpayapp.com/my/pricing) | RM1.30 | RM9.40 | – | RM2.20 | RM0.60 | 0 |
| [Stripe](https://stripe.com/en-my/pricing) | RM2.50 | RM16.00 | – | RM4.00 | – | 0 |
`–` = gateway tidak menyenaraikan kadar untuk kaedah itu. CHIP sahaja yang menyatakan SST 8% ke atas caj, jadi angka CHIP sudah termasuk SST. Laman toyyibPay tulis DuitNow QR "1.00% or RM 1.00" tanpa menyatakan yang mana satu; jadual guna 1%.

## Apa yang data ini tunjuk
- **FPX kadar tetap vs peratus:** Billplz, toyyibPay dan CHIP caj kadar tetap untuk FPX. HitPay dan Stripe caj peratus, jadi kosnya naik bila jumlah bayaran besar.
- **Billplz Standard (RM999 setahun)** hanya berbaloi kalau anda terima lebih kurang **167 bayaran FPX sebulan** atau lebih.
- Kadar boleh berubah. Sentiasa semak laman sumber (pautan dalam jadual) sebelum memilih.

## Fail
- `fees.json`: semua gateway, kadar setiap kaedah (`percent`, `fixed_rm`), yuran tahunan, SST dan pautan sumber.
- `fees.csv`: data yang sama, satu baris untuk setiap gateway dan kaedah.

Kaedah: `fpx_b2c` (FPX akaun peribadi), `fpx_b2b` (FPX korporat), `card` (kad tempatan), `duitnow_qr`.
Formula: `caj = jumlah × percent / 100 + fixed_rm`, kemudian × 1.08 jika `sst_on_fees` ialah `true`.

## Nota
Tiada kaitan dengan mana-mana gateway dan tiada pautan affiliate. Untuk langkah memasang FPX dalam website, baca [cara integrate FPX dalam website](https://miraclemikhael.com/ms/panduan/cara-integrate-fpx-website).

Diselenggara oleh [Miracle Mikhael](https://miraclemikhael.com), studio web & sistem di Petaling Jaya. Data: CC BY 4.0 (sila nyatakan sumber).
