# PrakPemin-A_Tugas2
A. MongoDB Compass
1. Lakukan koneksi ke MongoDB menggunakan connection string (disini saya secara lokal)
   ![Screenshot 2023-09-20 125255](https://github.com/askenas/PrakPemin-A_Tugas2/assets/134838656/def8d5d1-03e1-4437-ad4e-e4c23a33a697)

2. Buat database dengan melakukan klik “Create Database”
   ![Screenshot (373)](https://github.com/askenas/PrakPemin-A_Tugas2/assets/134838656/20540c5d-9683-4e68-9b68-98bfa0186206)

3. Lakukan insert buku pertama dengan melakukan klik “Add Data”, pilih “Insert
Document”, isi dengan data yang diinginkan dan klik “Insert”
![Screenshot 2023-09-20 125859](https://github.com/askenas/PrakPemin-A_Tugas2/assets/134838656/08c56bb2-382f-4ac4-b638-44ede4be6967)

4. Lakukan insert buku kedua dengan cara yang sama.
   ![Screenshot 2023-09-20 130523](https://github.com/askenas/PrakPemin-A_Tugas2/assets/134838656/376aa03b-7f01-47b6-8859-0b3f53de3195)

5. Lakukan pencarian buku dengan author “Osamu Dazai” dengan mengisi filter yang
diinginkan dan klik “Find”
![Screenshot 2023-09-20 130523](https://github.com/askenas/PrakPemin-A_Tugas2/assets/134838656/cbb02f99-32a4-4bd1-8fce-0931ff456607)

6. Lakukan perubahan summary pada buku “No Longer Human” menjadi “Buku yang
bagus (<NAMA>,<NIM>) dengan melakukan klik “Edit Document” (berlambang
pensil), mengisi nilai summary yang baru, dan melakukan klik “Update”
![Screenshot 2023-09-20 130712](https://github.com/askenas/PrakPemin-A_Tugas2/assets/134838656/c7fdb961-bfd0-4268-a2ed-2815bed00a72)

7. Lakukan penghapusan pada buku “I Am a Cat” dengan melakukan klik “Remove
Document” (berlambang tong sampah) dan melakukan klik “Delete”
![Screenshot 2023-09-20 130737](https://github.com/askenas/PrakPemin-A_Tugas2/assets/134838656/f7423ef0-fe64-4381-82dd-1ca16bfdb648)

B. MongoDB Shell

1. Lakukan koneksi ke MongoDB Server dengan menjalankan command mongosh bagi
yang menggunakan terminal build in OS sehingga tampilan terminal kalian akan
menjadi seperti berikut
![Screenshot 2023-09-20 131439](https://github.com/askenas/PrakPemin-A_Tugas2/assets/134838656/e87af12a-6c0f-4cdc-b250-cb3dde6b3f2a)

2. Mencoba melihat list database yang ada di server dengan menjalankan command
show dbs
![Screenshot 2023-09-20 131532](https://github.com/askenas/PrakPemin-A_Tugas2/assets/134838656/30df2465-2e65-452e-abeb-9b223e02ae87)

3. Untuk berpindah ke database “bookstore” gunakan command use bookstore , kalian
dapat memastikan telah berpindah ke database yang benar dengan melihat tulisan
sebelum tanda “>”
![Screenshot 2023-09-20 131611](https://github.com/askenas/PrakPemin-A_Tugas2/assets/134838656/0ba133f0-1ea4-46f1-abbd-a5bd31e156bd)

4. Cobalah untuk melihat collection yang ada pada database tersebut dengan
menggunakan command show collections
![Screenshot 2023-09-20 131611](https://github.com/askenas/PrakPemin-A_Tugas2/assets/134838656/84519293-c349-44b8-b9a0-ab9b44e04ff8)

5. Lakukan insert buku “Overlord I” dengan menggunakan command
db.books.insertOne(<data kalian>) , setelah insert buku berhasil maka MongoDB akan
mengembalikan pesan sebagai berikut.
![Screenshot 2023-09-20 132013](https://github.com/askenas/PrakPemin-A_Tugas2/assets/134838656/7d8acd36-b3c0-4642-a3d7-4083758dc85f)

6. Lakukan insert buku “The Setting Sun” dan “Hujan” dengan insert many dengan
menggunakan command db.books.insertMany(<data kalian>) , dan akan
![Screenshot 2023-09-20 133003](https://github.com/askenas/PrakPemin-A_Tugas2/assets/134838656/41a0d7b1-54da-4d9a-a7b5-a44809226238)

7. Lakukan pencarian buku dengan menggunakan command db.books.find() untuk
melakukan pencarian semua buku.
![Screenshot 2023-09-20 133155](https://github.com/askenas/PrakPemin-A_Tugas2/assets/134838656/309aa792-6375-4aa9-8792-71823fe5ef9c)

8. Tampilkan seluruh buku dengan author “Osamu Dazai” dengan mengisi argument
pada find() dengan menggunakan command db.books.find({<filter yang ingin
diisi>})
![Screenshot 2023-09-20 133312](https://github.com/askenas/PrakPemin-A_Tugas2/assets/134838656/36b56f32-871e-4629-afe5-2ea5e881f951)

9. Lakukan perubahan summary pada buku “Hujan” menjadi “Buku yang bagus
(<NAMA>,<NIM>) dengan mengunakan command db.books.updateOne({<filter>},
{$set: {<data yang akan di update>}}) sehingga output yang dihasilkan oleh MongoDB
akan menjadi seperti berikut
![Screenshot 2023-09-20 133725](https://github.com/askenas/PrakPemin-A_Tugas2/assets/134838656/f9d9f88a-c90c-44bd-beef-93042c24181a)

10. Lakukan perubahan publisher menjadi “Yen Press” pada semua buku “Osamu
Dazai” dengan menggunakan command db.books.updateMany({<filter>}, {$set: {<data
yang akan di update>}})
![Screenshot 2023-09-20 134100](https://github.com/askenas/PrakPemin-A_Tugas2/assets/134838656/72637abc-2bbf-4162-a153-884aec489513)

11. Lakukan penghapusan pada buku “Overlord I” dengan menggunakan command
db.books.deleteOne({<argument>})
![Screenshot 2023-09-20 134420](https://github.com/askenas/PrakPemin-A_Tugas2/assets/134838656/b239c86b-8009-413d-99de-5b0a68555901)

12. Lakukan penghapusan pada semua buku “Osamu Dazai dengan menggunakan
command db.books.deleteMany({<argument>})
![Screenshot 2023-09-20 134541](https://github.com/askenas/PrakPemin-A_Tugas2/assets/134838656/5a24a2a9-472e-432c-a789-122b179e9661)





