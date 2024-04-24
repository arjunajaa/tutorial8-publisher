### Modul 8 - Publisher

#### **Refleksi**

**a. Berapa banyak data yang akan dikirimkan oleh program publisher Anda ke message broker dalam satu kali jalankan?**

Publisher akan mengirimkan 5 data ke message broker dalam satu kali jalankan. Ini didasarkan pada 5 panggilan ke `publish_event` dalam fungsi utama di `src/main.rs`. Setiap panggilan akan mengirimkan `UserCreatedEventMessage` ke message broker.

**b. Apakah arti dari URL "amqp://guest:guest@localhost:5672" sama dengan program subscriber, apa maksudnya?**

URL `amqp://guest:guest@localhost:5672` adalah connection string untuk message broker. Karena connection string pada publisher dan subscriber sama, hal ini berarti keduanya terhubung ke message broker yang sama. Hal ini memungkinkan publisher untuk mengirim pesan ke broker, dan subscriber untuk menerima pesan tersebut dari broker.

**screenshot rabbitMQ management**
![Screenshot](image.png)

**screenshot terminal**
![docker](image-1.png)
![publisher](image-2.png)
![subscriber](image-3.png)

**screenshot memantau publisher**
![publisher1](image-4.png)
Apabila perintah cargo run dijalankan secara berulang dalam satu detik, kita akan melihat peningkatan yang signifikan dalam laju "Publish" pada periode tersebut, yang tercermin dalam puncak-puncak pada grafik.

Sebaliknya, apabila perintah cargo run hanya dijalankan sekali dalam satu detik, laju "Publish" akan menurun pada periode tersebut, sebagaimana ditunjukkan oleh lembah-lembah pada grafik.

Dari fenomena ini, dapat disimpulkan bahwa tingkat pesan yang diterima oleh message broker RabbitMQ akan berfluktuasi seiring dengan peningkatan jumlah pesan yang diterbitkan oleh publisher dalam periode waktu tertentu. Semakin banyak pesan yang diterbitkan dalam satu detik, semakin tinggi tingkat pesan yang ditampilkan pada grafik.
