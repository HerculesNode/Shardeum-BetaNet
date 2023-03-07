# Shardeum Betanet 1.1 Güncel Kurulum Rehberi - Hercules
![image](https://user-images.githubusercontent.com/101635385/216447120-a1add722-5d7d-4403-b2a9-85ef054ba631.png)



 ## 🟢 Linkler:

 * [Hercules Telegram](https://t.me/HerculesNode)
 * [Hercules Twitter](https://twitter.com/Hercules4413)
 
 

 ## 🟢 Sistemi Gereksinimleri

* Ekip tarafından önerilen  <br>
16 GB ram, 4+ GB sanal bellek önerilir<br>
60 GB ssd depolama alanı



## 🟢 Sistemi Güncelleme

Screen oluşturalım Shardeum yazan yere istediğinizi yazabilirsiniz.

```shell
screen -S shardeum
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


İlk defa kurulum yapacak olanlar Cüzdan sıfırlama ve eski kurulumu kaldırma adımını yapmasına gerek yoktur. <br> 


#### Matemask cüzdanımızı sıfırlıyoruz.  Ayarlar / Gelişmiş / Hesabı sıfırla  <br><br> 

![image](https://user-images.githubusercontent.com/101635385/219121810-9d6889b2-6893-4c9d-a0a4-433b2fff9dce.png)


<br><br>

## 🟢  Daha önceki kurulumu kaldırıyoruz.

```shell
cd ~/.shardeum
```

```shell
./cleanup.sh
```

```shell
cd ~/
```

```shell
rm -rf .shardeum
```

```shell
rm installer.sh
```


## 🟢 Yeni Kuruluma başlıyoruz.


```shell
curl -O https://gitlab.com/shardeum/validator/dashboard/-/raw/main/installer.sh && chmod +x installer.sh && ./installer.sh
```


Aşağıdaki sorulara cevap verin 

* By running this installer, you agree to allow the Shardeum team to collect this data. (y/n)?: y <br> 
 
* Do you want to run the web based Dashboard? (y/n): (y yazın) <br> 

* Set the password to access the Dashboard ( ŞİFRE GİRİN ) Bu Explorer üzerinden panele bağlanma şifreniz olacak unutmayın. <br> 

* Enter the port (1025-65536) to access the web based Dashboard (default 8080):  ( Direk Enter tuşuna basın yada başka port yazın Tavsiye 8080 kullanmanız ) <br> 

* This allows p2p communication between nodes. Enter the first port (1025-65536) for p2p communication (default 9001): Enter basın <br> 

* Enter the second port (1025-65536) for p2p communication (default 10001): Enter <br> 

* What base directory should the node use (defaults to ~/.shardeum): bir şey yazmayın enter basıp geçin <br> 


#### Gerekli kurulumlar başlayacak ve sonunda aşağıdaki resimdeki gibi bir çıktı görürseniz kurulum bitti demektir.  <br> 

![image](https://user-images.githubusercontent.com/101635385/216449058-387d47b5-d6ef-423d-8501-4490f11c1c5f.png)


## 🟢 3. Adım Doğrulayıcı

```shell
cd
```

```shell
cd .shardeum
```

```shell
./shell.sh
```

```shell
operator-cli gui start
```

Artık budan sonraki işlemler Explorer üzerinden 


## 🟢 4. Explorer işlemleri.

https://NODEIPADRESINIZ:8080   ( chrome yada hangi tarayıcıyı kullanıyorsanız node ip adresiniz ve port girdiğinizde aşağıdaki resimdeki gibi bir ekran gelecektir. 

![image](https://user-images.githubusercontent.com/101635385/216449601-78112f06-5d93-41a2-a737-1826ee770529.png)

<br>


#### ilk olarak Maintenance alanına tıklıyoruz. Burada aşağıdaki resimde bulunan beyaz butona basın ve nodeyi çalıştırın. Biraz bekleyin ve sayfayı yenileyin 1. Kutucuktaki gibi bir uyarı görürseniz nodeniz çalışıyor demektir.  <br>


![image](https://user-images.githubusercontent.com/101635385/216450237-e595b7cd-97bc-4c13-843f-ec39586653a8.png)

![image](https://user-images.githubusercontent.com/101635385/216528434-df065848-606d-4bee-a1fd-cc07f9e80b42.png)




## 🟢 5. Cüzdan bağlama

Kullanılacak ağ : Sphinx 1.X 

Aşağıdaki ağı Matemask cüzdanınıza ekleyiniz.

Ağ : Shardeum Sphinx 1.X <br>
New RPC URL : 	https://sphinx.shardeum.org/ <br>
Chain ID : 	8082 <br>
symbol : SHM <br>
Block Explorer URL :	https://explorer-sphinx.shardeum.org/ <br><br>


![image](https://user-images.githubusercontent.com/101635385/216532850-1c35b90f-d245-4be9-adf8-6c526d1c5ee3.png)





## 🟢 6. Faucet ve Stake Etme 


1- Discord Sunucusuna girin ve #faucet-1-1 kanalından SHM token alabilirsiniz. 

 * [Discord FAUCET](https://discord.gg/shardeum)

![image](https://user-images.githubusercontent.com/101635385/219289164-5ce047bb-7a30-41d3-84a3-a40eaa2b5934.png)

![image](https://user-images.githubusercontent.com/101635385/216561514-37ab1ead-9801-421e-939b-459d93f9807b.png)



2 - [Twitter FAUCET](https://faucet-sphinx.shardeum.org/?_ga=2.223730200.2098418439.1675365683-1010477743.1666250200)

#### Faucetten tweet atın 15 SHM gelecek hesabınıza 

![image](https://user-images.githubusercontent.com/101635385/216525966-93d207b1-910c-4dbe-a787-65a85439c99a.png)



#### Cüzdanınıza 15 SHM geldikten sonra ADD STAKE diyerek stake işlemini bitirebilirsiniz.  <br>


![image](https://user-images.githubusercontent.com/101635385/216532101-ca0e4aca-4422-42be-8241-51b723f92dc0.png)





## 🟢 7. Durum kontrol etme

#### Stake işlemini yaptıysanız aşağıdaki gibi bir ekran göreceksiniz. Active yazısı görünmüyorsa sayfayı yenileyin.


![image](https://user-images.githubusercontent.com/101635385/216527473-e8dc8f51-9b7d-4594-82b8-970ef71538c6.png)


## 🟢 Nominate key sorunu çözümü

![image](https://user-images.githubusercontent.com/101635385/219161856-c2ad942b-f923-4d1d-a5f7-d8f2f7966e47.png)


```shell
curl -O https://gitlab.com/shardeum/validator/dashboard/-/raw/main/installer.sh && chmod +x installer.sh && ./installer.sh
```





 ## 🟢 8080 port

Bu komut ile 8080 portta çalışan başka bir node varmı diye önce kontrol edin. 

```shell
 lsof -i -P -n | grep LISTEN
```



 ## 🟢 ip 0.0.0.0 hatası alırsanız çözümü

Bu komut ile 8080 portta çalışan başka bir node varmı diye önce kontrol edin. 

```shell
cd ~/.shardeum
```

```shell
./shell.sh
```

Bu adresten ip adresinizi öğrenin.

```shell
curl https://ipinfo.io/ip
```

Aşağıdaki komuta ip adresinizi yazın.

```shell
operator-cli set external_ip IPADRESINIZ
```
Aşağıdaki komuta nodu kurarken yazdığınız external port bilgibizi yazın. ( default 9001)
```shell
operator-cli set external_port PORTUNUZ
```
Gui'yi başlatın
```shell
operator-cli gui start
```
Ardından (https://NODEIPADRESINIZ:8080 ( chrome yada hangi tarayıcıyı kullanıyorsanız node ip adresiniz ve port girdiğinizde) sayfaya gidip Maintenance kısmından node unuzu Start edin.


 ## 🟢 Güncelleme 1.1.1 - 22.02.2023 

1- Nodu durdurun - STOP  <br>
2- Unstake yapın 

3-

```shell
cd ~/.shardeum
```

```shell
./shell.sh
```

```shell
exit
```

```shell
cd
```

```shell
curl -O https://gitlab.com/shardeum/validator/dashboard/-/raw/main/installer.sh && chmod +x installer.sh && ./installer.sh
```

4- Nodunuzu tekrar başlatın <br>
5 Tekrar 10 SHM stake yapın.



 ## 🟢 Shardeum Güncelleme 1.1.2 - 07.03.2023

1- Unstake yapın - Yapamıyorsanız yeni bir cüzdan oluşturun ve 10 SHM faucetten alın
2- Panelde Nodeyi durdurun STOP NODE



```shell
cd ~/.shardeum
```

```shell
docker stop shardeum-dashboard
```

```shell
curl -O https://gitlab.com/shardeum/validator/dashboard/-/raw/main/installer.sh && chmod +x installer.sh && ./installer.sh
```


4- Panel şifrenizi girin.
5- Portlara onay verin

<br>

```shell
cd .shardeum
```

```shell
./shell.sh
```

```shell
operator-cli gui start
```

Artık budan sonraki işlemler Explorer üzerinden

6- Nodunuzu tekrar başlatın <br>
7- Tekrar 10 SHM stake yapın.







Forklamayı ve beğenmeyi unutmayınız :)




