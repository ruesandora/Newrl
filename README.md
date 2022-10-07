<h1 align="center"> Newrl </h1>

![image](https://user-images.githubusercontent.com/101149671/194660242-7679c111-df7a-49fd-b9eb-1d83cd5e010f.png)

# Selamlar, Newrl chain testnet rehberi:

 * Ödül hakkında bilgi almak için [buraya](https://newrl.medium.com/join-newrls-incentivized-testnet-and-earn-newrl-tokens-716e6af7b1b9) tıkla. Not: bizim Buray değil.
 * Proje hakkında sorularınız için [buradayım](discord.gg/ruescommunity)
 * Projenin discord kanal [linki](https://discord.gg/GWVZxuH2)

## Sistem gereksinimleri:

 * Net bilgi yok, kendim test ettim:

```
4 CPU
8 RAM
80 GB SSD
```

## Sunucumuzu güncelliyoruz:
```
sudo apt-get update && sudo apt-get upgrade
```

## Git yüklüyoruz
```
git clone https://github.com/git/git
```

## Python3.7+  yüklüyoruz
```
sudo apt update && sudo apt install python3.10-venv
```

## Python3 Pip ve venv yüklüyoruz  
```
sudo apt update
sudo apt install python3-venv python3-pip
```

## Kurulum
```
git clone https://github.com/newrlfoundation/newrl.git
cd newrl
scripts/install.sh testnet
```

## Düğümü başlatıyoruz
```
apt install screen
```

```
screen -S newrl
```

```
scripts/start.sh testnet
```

## Node içinde oluşturduğumuz adresi Wallete tanımlama:

 * Aşağıdaki komuttan sonra sırayla:
 * testnet yazıyoruz + enter
 * Y yapıp enterlayıp çıkan çıktıyı kaydedin bu sizin json dosyanızdır.

```
cd newrl
python3 scripts/show_wallet.py
```

![image](https://user-images.githubusercontent.com/101149671/194666768-2920d230-3f2f-4fbe-89ff-84fc222bfb00.png)

## Şimdi [wallet sayfasını](https://wallet.newrl.net/) açıp az önce aldığımız dosyayı direk buraya yapıştırıp cüzdan oluşturuyoruz:

 * Sırasıyla:
 * Bir şifre oluşturuyoruz
 * İmport wallet diyoruz
 * Yukarıda kopyaladığımız {"public": "88e9e02....125e9169"} metni çıkan yere yapıştıralım

![image](https://user-images.githubusercontent.com/101149671/194667767-46220e17-1781-4e47-8910-b9032b478c05.png)

## İmport ettikten sonra KYC istiyor ama çakma KYC :D , nasıl mı? 

 * Göreslde gördüğünüz gibi seçenekleri random seçiyorum
 * KYC resmi ekle diyor ama ben Stride logosunu ekliyorum
 * Daha sonra activate wallet diyorum
 * İsteyen KYC verebilir ama seçeneklerde Türkiye yok :)
 * Ben KYC vermedim.

![image](https://user-images.githubusercontent.com/101149671/194668370-00e67a20-487f-4985-ad6d-42bc0ecb8894.png)


## Faucetten token alıyoruz:

 * Faucet [Linki](https://wallet.newrl.net/faucet/)
 * 500100 yapıp fund diyoruz

## Daha sonra tıpkı wormholes gibi cüzdandan validator oluşturuyoruz:

 * Sol üstten Run a node diyoruz

![image](https://user-images.githubusercontent.com/101149671/194668698-21b4dd15-bd86-498b-964f-be3ec1c828e1.png)

## Stake ediyoruz:

![image](https://user-images.githubusercontent.com/101149671/194668779-d0f8abb5-bfe5-4f01-9cd5-9765a358ea00.png)


## Validatörümüzü kontrol ediyoruz:

 * Altta ki komutun sonuna cüzdan adresinizi girin
 * Boş bir sekmeye yapıştırın
 * Succses diyorsa görselde ki gibi işlem tamam

```
http://archive1-testnet1.newrl.net:8421/sc-state?table_name=stake_ledger&contract_address=ct1111111111111111111111111111111111111115&unique_column=wallet_address&unique_value=CÜZDAN ADRESİ
```

![image](https://user-images.githubusercontent.com/101149671/194668964-532a33d3-2143-4a72-b022-bae7aa038d46.png)
