# Langkah - langkah ETL Prosess melalui Rapid Miner

![RapidMiner](https://yt3.ggpht.com/ytc/AKedOLSZzua1G6iU99tly9DfZL0GsyCQeONKPxm7UU2INg=s88-c-k-c0x00ffffff-no-rj)

# Persiapan 	:

- Mempunya Laptop atau PC
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

11. Lalu klik tombol save, untuk menyimpan koneksi yang telah anda buat.

![image](https://user-images.githubusercontent.com/56377742/159734895-ab275c54-6ad4-4787-8dc7-6d816ac0f094.png)

12. Selamat koneksi database anda telah selesai.

![image](https://user-images.githubusercontent.com/56377742/159735162-89ed3673-eee2-4632-893d-d6f6b9c36f34.png)


# Proses Penarikan data di Twitter 	:

1. Drag koneksi yang telah anda buat di Tab Process dengan Rapid Miner

![image](https://user-images.githubusercontent.com/56377742/159738196-e9d3d9a5-e514-4f8b-bb42-76fba48cc7a5.png)

2. Lalu ketik Search twitter di operators dan drag/Tarik ke process

![image](https://user-images.githubusercontent.com/56377742/159740776-d67794a9-6878-4fe6-aa83-548748042b07.png)

3. Klik search twitter dan klik show advanced parameters

![image](https://user-images.githubusercontent.com/56377742/159741200-ed84ea3e-04c7-4ce6-a76d-3971fc4320e5.png)

4. Lalu Isi parameter, query = id twitter yang ingin anda colect datanya, result type = recent or popular, limit = 1000, language = in (indonesia) dan datenya untuk menentukan sampai tanggal berapa untuk di query. Note : language diisi dengan huruf kecil.

![image](https://user-images.githubusercontent.com/56377742/159747191-a1ae123b-32cc-445f-9d51-4c8bf2b2ca69.png)

5. Kemudian Hubungkan out koneksi twitter ke con search twitter, seperti gambar dibawah ini :

![image](https://user-images.githubusercontent.com/56377742/159748241-08227cf6-25ae-4719-a0d6-1b0719df282b.png)

6. Lalu ketik di bagian Search tab Operators lalu cari "Select Attributes" dan drag/Tarik ke form process

![image](https://user-images.githubusercontent.com/56377742/159749046-1fbf52a6-7895-4730-892f-f425b36052e0.png)

7. Selanjutnya Hubungkan out "search twitter" ke exa "select attributes", dan Klik select attributes lalu ke parameter, ubah Attribute filter type menjadi "single" dan masukan attributes sesuai yg diinginkan , in case "text".


![image](https://user-images.githubusercontent.com/56377742/159749779-c34e7e9e-3d08-41e9-b817-cdf7960271f1.png)

8. Lalu car "Remove Duplicates" di operators dan drag/Tarik ke dorm process, (fungsi dari remove duplicates adalah, untuk menghapus record yang duplicate/sama).

![image](https://user-images.githubusercontent.com/56377742/159750651-763a7db9-f3ac-43ee-b8e0-d8f4504c8046.png)

9. Kemudian hubungkan exa select attributes ke exa Remove Duplicates untuk menjalankan proses tersebut.

![image](https://user-images.githubusercontent.com/56377742/159750959-532e8a1f-5b5c-4c47-89b1-aa051f85602d.png)

10. Setelah itu cari "Write CSV" di Tab operators kemudian drag/Tarik ke form process, untuk menjalankan proses penarikan data menjadi CSV file.

![image](https://user-images.githubusercontent.com/56377742/159751632-822ae27c-3269-40a4-a09a-a0ddb0089552.png)

11. Kemudian hubungkan exa Remove Duplicates ke input write CSV

![image](https://user-images.githubusercontent.com/56377742/159752233-e0b35a90-e0a3-4856-aaad-a51f2103d3fc.png)

12. Setelah itu hubungkan thr write CSV ke res

![image](https://user-images.githubusercontent.com/56377742/159752542-55663fab-7b12-423f-a140-4157ce3a97e3.png)

13. Klik write CSV lalu ke parameter dan browse untuk menentukan tempat penyimpanan data.

![image](https://user-images.githubusercontent.com/56377742/159752818-bed06588-dc97-42a0-8d47-8b441b44040f.png)

14. Lalu sesuaikan tempat penyimpanan file CSV anda, dan jangan lupa tentukan nama file CSV anda untuk di simpan di folder yang sudah anda pilih.

![image](https://user-images.githubusercontent.com/56377742/159753267-49f94630-addc-4f36-ac44-14e00e0157a2.png)

15. Jika sudah selesai Klik "Run process" dan lihat hasil data yang didapat akan langsung tersimpan di tempat penyimpanan/folder anda.

![image](https://user-images.githubusercontent.com/56377742/159754184-7b7c69b7-93a3-4388-a822-f406bca6d7ab.png)






