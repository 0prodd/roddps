# script by rodd
 
# install
yum -y install squid
yum -y install nano
yum -y install firewald
 
# process
systemctl enable squid.service
# process
firewall-cmd --zone=public --add-service=squid --permanent
# process
firewall-cmd --reload
# restart
systemctl restart squid
