### Modul 8 - Publisher

#### **Refleksi**

**a. Berapa banyak data yang akan dikirimkan oleh program publisher Anda ke message broker dalam satu kali jalankan?**

Publisher akan mengirimkan 5 data ke message broker dalam satu kali jalankan. Ini didasarkan pada 5 panggilan ke `publish_event` dalam fungsi utama di `src/main.rs`. Setiap panggilan akan mengirimkan `UserCreatedEventMessage` ke message broker.

**b. Apakah arti dari URL "amqp://guest:guest@localhost:5672" sama dengan program subscriber, apa maksudnya?**

URL `amqp://guest:guest@localhost:5672` adalah connection string untuk message broker. Karena connection string pada publisher dan subscriber sama, hal ini berarti keduanya terhubung ke message broker yang sama. Hal ini memungkinkan publisher untuk mengirim pesan ke broker, dan subscriber untuk menerima pesan tersebut dari broker.

**screenshot rabbitMQ management**
![Screenshot](image.png)
