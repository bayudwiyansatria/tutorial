```
sudo chcon -R -t httpd_sys_rw_content_t ../myRepo
```

```
sudo setsebool httpd_can_network_connect on
```
```
sudo setsebool -P httpd_can_network_connect on
```
```
/usr/sbin/getenforce 
```
```
/usr/sbin/setenforce Permissive
```
```
/usr/sbin/sestatus 
Output :
root@ls:~# /usr/sbin/sestatus 
SELinux status:                 enabled
SELinuxfs mount:                /selinux
Current mode:                   permissive
Mode from config file:          enforcing
Policy version:                 21
Policy from config file:        targeted
```