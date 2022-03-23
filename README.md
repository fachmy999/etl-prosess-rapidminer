# Langkah - langkah ETL Prosess melalui Rapid Miner

![RapidMiner](https://yt3.ggpht.com/ytc/AKedOLSZzua1G6iU99tly9DfZL0GsyCQeONKPxm7UU2INg=s88-c-k-c0x00ffffff-no-rj)

# Persiapan 	:

- Mempunyai akun twitter
- Download dan install software Rapid Miner di internet dengan link : https://my.rapidminer.com/nexus/account/index.html#downloads .

![image](https://user-images.githubusercontent.com/56377742/159726365-22e277ae-5895-473e-87bf-116be82abe50.png)

# Proses Koneksi Database :

1. di tab repository pilih Local Repository, Kemudian klik kanan Connection lali pilih Create Connection :

![image](https://user-images.githubusercontent.com/56377742/159727842-9a66abc3-d2f7-48e1-a656-20cdf2ca7603.png)

2. Pilih koneksinya mau koneksi apa (disini saya memilik koneksi lewat twiter)

![image](https://user-images.githubusercontent.com/56377742/159728267-4eac0aea-e954-43ba-8b5e-d5caf8210b3e.png)

3. Isikan nama koneksinya, disini saya beri nama Satgascovid19.id

![image](https://user-images.githubusercontent.com/56377742/159729108-0e458492-8766-468d-a531-2ba36c27f966.png)

4. Jika sudah pilih tombol create 

![image](https://user-images.githubusercontent.com/56377742/159729426-9d6ade75-fc3e-4813-9c90-b136dc19b03f.png)

5. Setelah itu pilih request token, dengan klik icon di samping access token seperti gambar di bawah ini :

![image](https://user-images.githubusercontent.com/56377742/159730108-3e29f460-241a-42a2-a26d-2a47bcfa4282.png)

6. Lalu klik request acces tokennya untuk mendapatkan kode akses token api twitter, (disini anda harus login akun twiter anda).

![image](https://user-images.githubusercontent.com/56377742/159730607-af96f6bc-a716-44a5-ae79-c65dad7f7429.png)

7. Setelah anda klik request tersebut, maka anda akan di direct ke akun twiter anda, lalu pilih authorize untuk mendapatkan kode akses token twitter anda.

![image](https://user-images.githubusercontent.com/56377742/159731297-97e4f263-7b8e-453e-939f-62ff47c8829a.png)

8. Lalu isikan kode access token twitter anda ke request kode rapid miner anda.

![image](https://user-images.githubusercontent.com/56377742/159732011-6ac1b1aa-bcec-4ebb-bb0f-ac19f860f130.png)

9. masukan kode tersebut seperti di gambar ini, lalu pilih complete

![image](https://user-images.githubusercontent.com/56377742/159732374-7a768427-8172-412c-891c-c6e2e0418211.png)

10. Jangan lupa testing koneksi anda sebelum menyelesaikan proses tersebut, pastikan koneksi berhasil seperti gambar di bawah ini :

![image](https://user-images.githubusercontent.com/56377742/159732912-6f5e712e-78af-4231-a086-16577b3b1ed0.png)

