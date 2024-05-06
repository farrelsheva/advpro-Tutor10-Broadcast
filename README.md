### Experiment 2.1
![Experiment 2.1](experiment2-1.png)

dengan websocket Tokio, client membuat sebuah connection websocket ke port 2000, dan membaca input dari pengguna secara asinkronus. Jika membaca sebuah message dari server, dia print message ke console, dan jika ada input pengguna, ia mengirim message melalui websocket.
Server merupakan broadcasting channel yang mempunyai transmitter bcast_tx, dan membuat sebuah listener pada address yang sama. untuk setiap koneksi baru dia membuat sebuah task aysnc yang menerima message dari client (`handle_connection`). Seperti minggu lalu dibahas `handle_conenction` memakai ws_stream untuk menerima message dari client dan mengirim message ke client dengan kontinu.

### Experiment 2.2

Dengan modifikasi pada kedua file, aplikasi masih jalan dengan lancar. Client masih bisa mengirim message ke server dan juga kebalikanya. 
![Experiment 2.2 #1](experiment2-2-1.png)

Modifikasi hanya pada server, membuat client tidak bisa menemukan server pada websocket. 
![Experiment 2.2 #2](experiment2-2-2.png)