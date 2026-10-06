# WEBGPU

#### Vast Kayıt : 

| Server Sağlayıcısı        | Kayıt Link              | Neden |
|------------------|----------------------------|----------------------------|
| **VAST GPU**          | [Link](https://cloud.vast.ai/?ref_id=228932) | İstediğimiz Sunucular / Kripto Ödeme |

- https://cloud.vast.ai/billing/ 'den Kripto yada Kart ile bakiye ekleyebilirsiniz.

## Bağlanmak için SSH Key Ayarlama : 

- Wsl Kullanıyorsanız CMD / Powershell - Mac'de Terminal Açın
```bash
ssh-keygen
```

![image](https://github.com/user-attachments/assets/ec8c9bac-3397-40da-ac0d-70bcb985a360)

- 3 Soru Yöneltiyor ; 
```bash
Enter file in which to save the key (/home/codespace/.ssh/id_rsa):
Enter passphrase (empty for no passphrase):
Enter same passphrase again: 
```
- İsim değiştirmek isterseniz (/home/codespace/.ssh/id_rsa): 'den sonra isim yazıp enter'e basın.
- Şifre'ye enter sonrakinede enter diyip geçebilirsiniz.

![image](https://github.com/user-attachments/assets/6e944f73-120c-44e1-9d29-d220352d9594)

- \home\kullanici\.ssh\id_rsa.pub 'ı açın. İçindekini kopyalayın.

-  https://cloud.vast.ai/manage-keys/ - + New'den kayıt edin keyinizi.

![image](https://github.com/user-attachments/assets/3a15ce26-341b-4ca9-8a7a-47d1cd3b927c)

## Kartımızı Seçelim - Giriş Yapalım; 

<img width="1293" height="793" alt="image" src="https://github.com/user-attachments/assets/77111451-8e89-4403-99d9-bda5fa860ebc" />


- Sol üst template NVIDIA CUDA seçili kaldı.
- Ucuzdu 4070S Tercih ettim.

#### Sunucumuza Erişelim;

<img width="642" height="219" alt="image" src="https://github.com/user-attachments/assets/90472012-366d-400c-8001-3f9cc2d4c8bf" />

- Instance sekmesine tıklayalım.

<img width="1210" height="411" alt="image" src="https://github.com/user-attachments/assets/caede46d-e473-4a13-b6e2-77e5f001dac7" />

- Sarıyla gösterdiğim CLI Simgesine tıklayın.

<img width="507" height="373" alt="image" src="https://github.com/user-attachments/assets/172bb4f6-0603-4086-bbdb-4d3b8d74b872" />

- Üstteki yada alttaki olur farketmez, üsttekiyle bağlandıysanız üstteki - alttakiyle bağlanırsa alttaki bazen sorun olabiliyor bende 2. yi kullanıyorum.

- Değiştirmemiz gereken bir şey var - Örnek Bu Benimki;

```bash
ssh -p 10705 root@179.255.154.131 -L 8080:localhost:8080
```

- Buradaki 8080'i 6080 Olarak Değiştiricez - Şöyle Olacak;


```bash
ssh -p 10705 root@179.255.154.131 -L 6080:localhost:6080
```

<img width="836" height="306" alt="image" src="https://github.com/user-attachments/assets/ef2ccad6-284f-478e-8db6-4ef99168f5c6" />

- Terminale yapıştırdık enterledik.
- Bize soru soruyor ; yes yazıyoruz ve enterliyoruz.

<img width="855" height="193" alt="image" src="https://github.com/user-attachments/assets/728583ce-6f06-48cf-947d-732134b2f85c" />

- Sunucudayız.

## Kurulum;

- Script'i İndirelim;

```bash
wget https://raw.githubusercontent.com/FurkanL0/keyfekeder/refs/heads/main/xorg/sandbox/setup-gpu-browser-vast.sh
```

<img width="961" height="345" alt="image" src="https://github.com/user-attachments/assets/2e3d0680-9bae-4e64-b7aa-2b250180eb32" />


- Yetki Verelim;

```bash
chmod +x setup-gpu-browser-vast.sh
```
<img width="581" height="146" alt="image" src="https://github.com/user-attachments/assets/442bd7da-2c03-4b67-a1a6-31558c858203" />


- Çalıştıralım;

```bash
sudo ./setup-gpu-browser-vast.sh
```

<img width="539" height="220" alt="image" src="https://github.com/user-attachments/assets/2c4f8a06-3e4f-41b5-b3b3-19edba1e3b4b" />

- 1

<img width="877" height="482" alt="image" src="https://github.com/user-attachments/assets/0e9e2ad8-bff6-4961-b8c5-28e3527053a3" />

- Kurulum başladı.

<img width="963" height="338" alt="image" src="https://github.com/user-attachments/assets/962bb751-f331-4664-9276-e4e568df422f" />

- Bu aşamada sizden ŞİFRE isteyecek.
- Yazsanızda görünmeyecek ama yazacak ( garip geliyor biliyorum ama böyle )
- Maximum 8 hane.

<img width="520" height="173" alt="image" src="https://github.com/user-attachments/assets/f18e0317-635e-445e-a744-d3f806b5ccf8" />

- Tekrar şifrenizi istiyor doğrulamak için yazın.

<img width="732" height="727" alt="image" src="https://github.com/user-attachments/assets/0adf6009-0c5a-4342-935c-dad0c5ab57b3" />

- Kurulum Başarılı.

## VNC'ye Erişelim;

- Kendi Tarayıcınızdan ( chrome - edge vb. vb. ) - bu adrese girin;

```bash
http://127.0.0.1:6080/vnc.html
```
<img width="710" height="543" alt="image" src="https://github.com/user-attachments/assets/f743d6bd-cacc-47ae-8fff-e02e9de66806" />

- Connect'e basın.

<img width="310" height="256" alt="image" src="https://github.com/user-attachments/assets/3fc3b7d3-eaf7-44de-b7d1-05ac144bfecc" />

- Ayarladığınız şifreyi girip butona basın.

<img width="989" height="978" alt="image" src="https://github.com/user-attachments/assets/aea09fd0-00f6-482d-9fb8-08bc685fff7e" />

- Bu kadar.
- Sunucu açık kaldığı sürece aktif kalır.

- Testler:
- 1: https://mprep.info/gpu/
- 2: https://ipaddress.si/
