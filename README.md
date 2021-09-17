#Proses instalasi membutuhkan root privilledges.<br>
#Berikut step by step proses  installasi agent monitoring<br>
#Pastikan semua hostname Server tidak ada yang sama karena system monitoring mengidentifikasi server berdasarkan hostname yang unik.<br>
1.Masuk ke directory dimana file git ini akan di simpan.misal <br>
git clone https://github.com/massyafaat/installagentmonitoring.git<br>
2.Masuk ke direktori instalasi<br>
cd installagentmonitoring/<br>
3.Berikan permission agar script bisa di execute.<br>
chmod +x install-agent.sh<br>
4.Jalan Proses instalasi<br>
./install-agent.sh<br>
5.Cek status service agent<br>
systemctl status telegraf<br>
6.Periksa log telegraf<br>
tail -100 /var/log/telegraf/telegraf.log<br>
7.Cek koneksi ke server monitoting<br>
telnet influxdb.ms-biznetgio.net 8086<br>
