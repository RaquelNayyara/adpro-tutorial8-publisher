# Tutorial 8 Publisher

#### Raquel Nayyara Aulia - 2206826583

### How many data your publlsher program will send to the message broker in one run?
Program publisher akan mengirimkan 5 data ke broker pesan dalam satu kali eksekusi

### The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?
URL `amqp://guest:guest@localhost:5672` menghubungkan ke broker AMQP yang beroperasi di mesin lokal, dengan protokol AMQP, autentikasi menggunakan username dan password default `guest`, dan broker berjalan di localhost

### Running RabbitMQ as message broker.
![Running RabbitMQ as message broker](assets/image/Running%20RabbitMQ%20as%20message%20broker.jpg)

### Sending and processing event
![Sending and processing event](assets/image/Sending%20and%20processing%20event.jpg)
Saat message broker seperti RabbitMQ sedang aktif, ketika kita menjalankan program Subscriber dan Publisher (dengan perintah `cargo run`), Publisher akan mengirimkan 5 event data ke message broker, dan Subscriber akan menerima data tersebut. Dalam gambar yang disajikan, terlihat bahwa Publisher mengirimkan data satu kali ke message broker, dan Subscriber menerima data tersebut

### Monitoring chart based on publisher
![Monitoring chart based on publisher](assets/image/Monitoring%20chart%20based%20on%20publisher.jpg)
Dari gambar, bisa dilihat message rates akan meningkat ketika Publisher mengirimkan data ke message broker. Jika message rates tinggi, maka message broker akan menerima banyak data dari Publisher.