#Proses instalasi membutuhkan root privilledges.
#Berikut step by step proses  installasi agent monitoring
#Pastikan semua hostname Server tidak ada yang sama karena system monitoring mengidentifikasi server berdasarkan hostname yang unik.
1.Masuk ke directory dimana file git ini akan di simpan.misal 
git clone https://github.com/massyafaat/installagentmonitoring.git
2.Masuk ke direktori instalasi
cd installagentmonitoring/
3.Berikan permission agar script bisa di execute.
chmod +x install-agent.sh
4.Jalan Proses instalasi
./install-agent.sh
5.Cek status service agent
systemctl status telegraf
6.Periksa log telegraf
tail -100 /var/log/telegraf/telegraf.log
7.Cek koneksi ke server monitoting
telnet influxdb.ms-biznetgio.net 8086
