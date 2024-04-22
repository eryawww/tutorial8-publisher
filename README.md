a. How many data your publlsher program will send to the message broker in one
run?

Berdasarkan kode yang disediakan, Publisher akan mengirimkan lima pesan dalam sekali run. Setiap pemanggilan fungsi `p.publish_event` akan mengirimkan satu pesan dengan setiap pesan adalah instance dari `UserCreatedEventMessage` dengan nilai `user_id` dan `user_name` yang berbeda.

b. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?

Alamat `amqp://guest:guest@localhost:5672` digunakan untuk menyambung ke sebuah message yang menggunakan protokol AMQP. Alamat yang sama ini berarti kedua program akan menyambung ke message broker yang sama. Seperti sebelumnya,
- `guest:guest` adalah nama pengguna dan kata sandi yang digunakan.
- `localhost` adalah hostname atau alamat IP dari mesin server dimana message broker berjalan. Dalam kasus ini, ia berjalan pada mesin yang sama.
- `5672` adalah nomor port dimana komunikasi akan didengarkan.

Jadi, baik publisher dan subsriber berinteraksi dengan message broker/server yang sama, mungkin pengiriman dan penerimaan pesan dari antrian yang sama.