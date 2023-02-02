# Shardeum Betanet Kurulum Rehberi - Hercules
![image](https://user-images.githubusercontent.com/101635385/216447120-a1add722-5d7d-4403-b2a9-85ef054ba631.png)



 ## 🟢 Linkler:

 * [Hercules Telegram](https://t.me/HerculesNode)
 * [Hercules Twitter](https://twitter.com/Hercules4413)


 ## 🟢 Faucet
 
 * [Discord](https://discord.gg/shardeum)

 Faucet SHM token için discord adresine girin oradan Faucet 1-6 ve Faucet-2-1 kanalına girin ve resimdeki gibi token alın
 
 ![image](https://user-images.githubusercontent.com/101635385/216453273-47c43ce8-93a2-4091-ab2d-f807ef62ac5f.png)

 komut : /faucet cüzdan adresiniz
 
 
 
  ## 🟢 8080 port

Bu komut ile 8080 portta çalışan başka bir node varmı diye önce kontrol edin. 

```shell
 lsof -i -P -n | grep LISTEN
```
 

 ## 🟢 Sistemi Gereksinimleri

* Ekip tarafından önerilen  <br>
16 GB ram, 4+ GB sanal bellek önerilir<br>
60 GB ssd depolama alanı



## 🟢 Sistemi Güncelleme

Screen oluşturalım Shardeum yazan yere istediğinizi yazabilirsiniz.

```shell
screen -S Shardeum
```


```shell
sudo apt-get install curl
```

```shell
sudo apt update
```

## 🟢 1. Adım Docker Kurulumu

```shell
sudo apt install docker.io
```

```shell
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```

```shell
sudo chmod +x /usr/local/bin/docker-compose
```



## 🟢 2. Adım Kurulum

```shell
curl -O https://gitlab.com/shardeum/validator/dashboard/-/raw/main/installer.sh && chmod +x installer.sh && ./installer.sh
```


Aşağıdaki sorulara cevap verin 

* Do you want to run the web based Dashboard? (y/n): y yazıp Enter 
* Set the password to access the Dashboard ŞİFRE GİRİN  Enter
* Enter the port (1025-65536) to access the web based Dashboard (default 8080): 8080 yazın enter
* What base directory should the node use (defaults to ~/.shardeum): bir şey yazmayın enter basın
* Select a network to connect to:  bu soru çıkarsa 2 yazıp enter


## 🟢 3. Adım Doğrulayıcı

```shell
cd .shardeum
```

```shell
./shell.sh
```

```shell
operator-cli gui start
```

Kurulum uzun sürecek aşağıdaki resimi görürseniz kurulum bitti demektir. Artık budan sonraki işlemler Explorer üzerinden 

![image](https://user-images.githubusercontent.com/101635385/216449058-387d47b5-d6ef-423d-8501-4490f11c1c5f.png)


## 🟢 4. Explorer işlemleri.

https://NODEIPADRESINIZ:8080   ( chrome yada hangi tarayıcıyı kullanıyorsanız node ip adresiniz ve port girerek aşağıdaki resimdeki gibi bir ekran gelecektir. 

![image](https://user-images.githubusercontent.com/101635385/216449601-78112f06-5d93-41a2-a737-1826ee770529.png)


* ilk olarak Maintenance alanına tıklıyoruz. Burada aşağıdaki resimde bulunan beyaz butona basın ve nodeyi çalıştırın. Biraz bekleyin ve sayfayı yenileyin 1. Kutucuktaki gibi bir uyarı görürseniz nodeniz çalışıyor demektir. 


![image](https://user-images.githubusercontent.com/101635385/216450237-e595b7cd-97bc-4c13-843f-ec39586653a8.png)

![image](https://user-images.githubusercontent.com/101635385/216450286-708edb1c-7417-4e47-9350-26bbb3e6958b.png)



## 🟢 5. Cüzdan bağlama

* Daha sonra Matemask cüzdanınızı bağlayın Ağ : Liberty 2 X eğer ağ yoksa chainlist. ekleyin 

Ağ ekleme : https://chainlist.org/?search=shardeum

![image](https://user-images.githubusercontent.com/101635385/216450617-274ae00c-74c1-44c2-8369-59d2bc8fb0c9.png)


## 🟢 6. Stake Etme

hesabınızda 10 SHM token olması gerekiyor. Token temin ettikten sonra aynı sayfa üzerinden cüzdanınızı bağlayın Add stake butonuna basın ve 10 SHM stake edin

![image](https://user-images.githubusercontent.com/101635385/216450969-95907158-9dd5-4021-947e-770c74ac847c.png)

![image](https://user-images.githubusercontent.com/101635385/216451080-6cf55c20-9561-4bd3-9f80-4be49dbc7d3f.png)




Forklamayı ve beğenmeyi unutmayınız :)




