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

## Kurulum;

- Script'i İndirelim;

```bash
wget https://raw.githubusercontent.com/FurkanL0/keyfekeder/refs/heads/main/xorg/sandbox/setup-gpu-browser-vast.sh
```

- Yetki Verelim;

```bash
chmod +x setup-gpu-browser-vast.sh
```

- Çalıştıralım;

```bash
sudo ./setup-gpu-browser-vast.sh
```
