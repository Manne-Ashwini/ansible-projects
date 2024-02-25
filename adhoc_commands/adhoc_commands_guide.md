1 Display hostname and IP address of all hosts:
```
ansible all -i inventory -m shell -a "hostname && ip addr show"
```
2 Check CPU information:
```
ansible all -i inventory -m shell -a "cat /proc/cpuinfo"
```

3 Check memory information (in gigabytes):
```
ansible all -i inventory -m shell -a "free -g"
```
4 Check disk usage:
```
ansible all -i inventory -m shell -a "df -h"
```
5 Check system uptime:
```
ansible all -i inventory -m shell -a "uptime"
```
6 Check network interface information:
```
ansible all -i inventory -m shell -a "ip link show"
```
7 Install a package (example with apt):
```
ansible all -i inventory -m apt -a "name=<package_name> state=present"
```
8 Remove a package (example with apt):
```
ansible all -i inventory -m apt -a "name=<package_name> state=absent"
```
9 Start a service:
```
ansible all -i inventory -m service -a "name=<service_name> state=started"
```
10 Stop a service:
```
ansible all -i inventory -m service -a "name=<service_name> state=stopped"
```
11 Create a file:
```
ansible all -i inventory -m file -a "path=/path/to/file.txt state=touch"
```
12 Delete a file:
```
ansible all -i inventory -m file -a "path=/path/to/file.txt state=absent"
```
13 Create a user:
```
ansible all -i inventory -m user -a "name=<username> state=present"
```
14 Delete a user:
```
ansible all -i inventory -m user -a "name=<username> state=absent"
```
15 Add SSH key to authorized_keys:
```
ansible all -i inventory -m authorized_key -a "user=<username> key='{{ lookup('file', '/path/to/public_key.pub') }}'"
```
16 Remove SSH key from authorized_keys:
```
ansible all -i inventory -m authorized_key -a "user=<username> key='{{ lookup('file', '/path/to/public_key.pub') }}' state=absent"
```
