#Cài đặt grafana
echo "deb https://packages.grafana.com/oss/deb stable main" | sudo tee -a /etc/apt/sources.list.d/grafana.list
wget -q -O - https://packages.grafana.com/gpg.key | sudo apt-key add
#
apt-get update
apt-get install grafana -y
#Khởi động lại dịch vụ grafana
systemctl start grafana-server
systemctl enable grafana-server.service
Truy cập trình duyệt với url http://172.16.69,201:3000
Tài khoản mặc định admin/admin
