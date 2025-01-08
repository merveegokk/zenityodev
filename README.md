# zenityodev
# Kullanıcı ve Ürün Yönetim Sistemi

Bu proje, Bash ve Zenity kullanarak kullanıcı ve ürün yönetimi yapan bir komut dosyasıdır. Kullanıcılar için güvenlik özellikleri ve etkileşimli bir grafik arayüz sunar.

---

## Özellikler

- Kullanıcı girişi (admin ve user rolleri).
- Kullanıcı ekleme, güncelleme ve listeleme.
- Ürün ekleme, güncelleme, silme ve listeleme.
- Loglama (işlemler ve hatalar kaydedilir).
- Güvenli şifre saklama (SHA-256 hash ile).

---

## Gerekli Kurulumlar

- **Zenity:** Grafiksel arayüz oluşturmak için gereklidir. Aşağıdaki komutla kurabilirsiniz:

```bash
sudo apt-get install zenity
```

- **Bash:** Çoğu Linux dağıtımında varsayılan olarak gelir.

---

## Nasıl Çalıştırılır?

1. Bu projeyi klonlayın veya indirin:

```bash
git clone https://github.com/kullanici/bash-inventory-management.git
cd bash-inventory-management
```

2. Scripti çalıştırmadan önce izin verin:

```bash
chmod +x script.sh
```

3. Scripti başlatın:

```bash
./script.sh
```

---

## Kullanım Rehberi

### Giriş Ekranı

Zenity penceresi üzerinden kullanıcı adı ve parola girerek giriş yapabilirsiniz.

![Başlıksız](https://github.com/user-attachments/assets/f0b3e06d-dfa5-4fae-94f9-145971931a64)
![WhatsApp Image 2025-01-08 at 16 26 43](https://github.com/user-attachments/assets/f065752d-8e6f-4985-811d-bb6a27e58a45)
![WhatsApp Image 2025-01-08 at 16 26 44](https://github.com/user-attachments/assets/3a4529d3-f97e-46d9-912f-5ac1f28a203a)


### Yönetici Menüsü

Admin rolüyle giriş yapıldığında aşağıdaki seçenekler sunulur:
- Ürün Ekle
- Ürün Listele
- Ürün Güncelle
- Ürün Sil
- Kullanıcı Yönetimi
- Program Yönetimi

![WhatsApp Image 2025-01-08 at 16 26 44(1)](https://github.com/user-attachments/assets/44b867c7-533e-4806-810e-fecfbdae19b9)
![WhatsApp Image 2025-01-08 at 16 26 44(2)](https://github.com/user-attachments/assets/8c0afb83-6cfd-44dd-95e0-20f1a6f74f57)

![WhatsApp Image 2025-01-08 at 16 26 48](https://github.com/user-attachments/assets/3efe5277-3462-40f2-ae06-b0d3a2bc4bad)
![WhatsApp Image 2025-01-08 at 16 26 49](https://github.com/user-attachments/assets/5cb5018d-24fd-40df-bd7a-fbafcb81a5d6)
![WhatsApp Image 2025-01-08 at 16 26 50](https://github.com/user-attachments/assets/12cb4a35-5d16-4444-b784-de927e66216f)
![WhatsApp Image 2025-01-08 at 16 26 50(1)](https://github.com/user-attachments/assets/abf5020f-74c0-4115-b237-fa5a49835297)
![WhatsApp Image 2025-01-08 at 16 26 50(2)](https://github.com/user-attachments/assets/77a3cc5c-d817-421b-9a2a-a663329eaf8d)


### Kullanıcı Menüsü

User rolüyle giriş yapıldığında daha sınırlı seçenekler sunulur:
- Ürün Listele
- Rapor Al
![WhatsApp Image 2025-01-08 at 16 38 59](https://github.com/user-attachments/assets/84dd6254-7a7a-4d76-b2cb-ab94fd2ce5dd)


### Ürün Ekleme

Ürün eklemek için formu doldurun:

![WhatsApp Image 2025-01-08 at 16 26 45(1)](https://github.com/user-attachments/assets/92297a56-e82d-486a-9833-b24d48c94ba6)
![WhatsApp Image 2025-01-08 at 16 26 46](https://github.com/user-attachments/assets/cd858729-5a8e-448e-b1b0-79bf2d87554b)
![WhatsApp Image 2025-01-08 at 16 26 46(1)](https://github.com/user-attachments/assets/d2af3503-ffd2-47a5-a6b3-a77ef286ba97)

![WhatsApp Image 2025-01-08 at 16 26 47](https://github.com/user-attachments/assets/fe4cfef1-63f5-4852-b46b-eb7ff9a11dbb)

### Ürün Listeleme

Depoda bulunan tüm ürünlerin bir listesini görüntüleyin:

![Ürün Listeleme](images/list_products.png)

---

## Loglama

Tüm işlemler ve hatalar `log.csv` dosyasına kaydedilir. Örnek log formatı:

```
2025-01-08 15:30:12 - Kullanıcı admin ürün ekledi: "Laptop"
2025-01-08 15:35:45 - Kullanıcı user hatalı parola girişi yaptı.
```

---
![WhatsApp Image 2025-01-08 at 16 42 49](https://github.com/user-attachments/assets/0ec2f660-d9ed-4ee3-bb1d-32a3dc1bdebc)



## Teknik Detaylar

### Kullanılan Teknolojiler
- **Bash Script:** Ana kontrol ve işlevler.
- **Zenity:** Grafiksel kullanıcı arayüzü.
- **SHA-256:** Şifrelerin güvenli bir şekilde saklanması.

### Dosya Yapısı
- `script.sh`: Ana komut dosyası.
- `depo.csv`: Ürün bilgilerini saklar.
- `kullanici.csv`: Kullanıcı bilgilerini saklar.
- `log.csv`: Loglama dosyası.

---
### Video

https://youtu.be/hCAOtC30zhI?si=-gb0lVu8ZDy9YzFB

## Katkıda Bulunun

Bu projeyi geliştirmek veya hataları bildirmek için katkıda bulunabilirsiniz. Lütfen bir **pull request** gönderin veya bir **issue** açın.

---

## Lisans

Bu proje MIT lisansı altındadır. Daha fazla bilgi için [LICENSE](LICENSE) dosyasına bakın.
