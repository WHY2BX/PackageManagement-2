# RPM (Red Hat Package Manager)
## RPM คืออะไร 
RPM (Red Hat Package Manager) เป็น default open source และเป็น utility ใน package management ที่ค่อนข้างได้รับความนิยมสำหรับคนที่ใช้ Red Hat (ex. RHEL, CentOS และ Fedora) โดย RPM เป็นเครื่องมือที่ช่วยทำให้ผู้ใช้งาน หรือผู้ดูแลระบบสามารถทำการ install, update, uninstall, query, verify รวมไปถึงจัดการ package ในระบบปฏิบัติการ Unix/Linux ได้

## Command พื้นฐาน
* **Install** : ใช้สำหรับติดตั้งแพ็คเกจ RPM
* **Remove** : ใช้เพื่อลบ หรือยกเลิกการติดตั้งแพ็คเกจ RPM
* **Update** : ใช้เพื่ออัปเดตแพ็คเกจ RPM ที่มีอยู่
* **Verify** : ใช้เพื่อตรวจสอบแพ็คเกจ RPM
* **Query** : ใช้ในการสืบค้นแพ็คเกจ RPM

## การ Check dependencies ก่อนติดตั้ง RPM
การตรวจ dependencies ก่อนติดตั้งจะช่วยป้องกันปัญหาที่อาจเกิดขึ้นในกระบวนการติดตั้งหรือในการใช้งานแพ็คเกจนั้น ๆ ในภายหลังได้
```
sudo rpm -qpR [ ชื่อ package ]
```
  * **q** – บอกให้ RPM ทำการค้นหาแพ็คเกจ
  * **p** – ระบุแพ็คเกจเป้าหมายที่จะค้นหา
  * **R** – นี่แสดง requirements สำหรับแพ็คเกจ
### Exxample
```
[root@tecmint]# rpm -qpR BitTorrent-5.2.2-1-Python2.4.noarch.rpm

/usr/bin/python2.4
python >= 2.3
python(abi) = 2.4
python-crypto >= 2.0
python-psyco
python-twisted >= 2.0
python-zopeinterface
rpmlib(CompressedFileNames) = 2.6
```
credit: https://www.tecmint.com/20-practical-examples-of-rpm-commands-in-linux/

# Install
ขั้นตอนแรกของการติดตั้ง RPM คือเราจะต้องดาวน์โหลดไฟล์ RPM มาก่อน โดยสามารถดาวน์โหลดได้ 2 วิธี
## Download RPM Files from the Internet
 * สามารถดาวน์โหลดไฟล์ RPM จากอินเทอร์เน็ตโดยใช้เว็บเบราว์เซอร์ หรือใช้คำสั่ง wget
```
wget [option] [URL]
```

## Download RPM Files from the Repository
 * สามารถใช้ yum และ dnf ช่วยให้เราสามารถดาวน์โหลดไฟล์ RPM ได้
```
sudo yumdownloader [package_name]
```
```
dnf download [package_name]
```


## Install RPM File
เมื่อเราดาวน์โหลดไฟล์ RPM มาเรียบร้อยแล้ว ขั้นตอนต่อไปคือการติดตั้ง สามารถทำได้ 3 วิธี โดยใช้คำสั่ง rpm, yum และ dnf
```
sudo rpm -i [package_name]
```
```
sudo yum localinstall [package_name]
```
```
sudo dnf localinstall [package_name]
```

## Check ว่าติดตั้ง rpm เรียบร้อยแล้ว
```
rpm -q  [ ชื่อ package ]
```
### Example
```
[root@tecmint]# rpm -q BitTorrent

BitTorrent-5.2.2-1.noarch
```
credit: https://www.tecmint.com/20-practical-examples-of-rpm-commands-in-linux/

## Remove
```
sudo rpm -e  [package_name]
```
## Example
```
[root@tecmint]# rpm -evv nx
```
credit: https://www.tecmint.com/20-practical-examples-of-rpm-commands-in-linux/

## Update
```
sudo rpm -Uvh [package_name]
```
### Example
```
[root@tecmint]# rpm -Uvh nx-3.5.0-2.el6.centos.i686.rpm
Preparing...                ########################################### [100%]
   1:nx                     ########################################### [100%]
```
credit: https://www.tecmint.com/20-practical-examples-of-rpm-commands-in-linux/

## Verify
ใช้ตรวจสอบ package RPM ทั้งหมด
```
sudo rpm -Va
```
### Example
```
[root@tecmint]# rpm -Va

S.5....T.  c /etc/rc.d/rc.local
.......T.  c /etc/dnsmasq.conf
.......T.    /etc/ld.so.conf.d/kernel-2.6.32-279.5.2.el6.i686.conf
S.5....T.  c /etc/yum.conf
S.5....T.  c /etc/yum.repos.d/epel.repo
```

## Query
ค้นหาไฟล์ของ RPM package
```
rpm -qf [ query name]
```
ค้นหาข้อมูลของ package นั้น
```
rpm -qi [ query name]
```
ค้นหา document ของ package นั้น
```
rpm -qdf (query document file)
```


# All reference
1) https://www.tecmint.com/20-practical-examples-of-rpm-commands-in-linux/

2) https://phoenixnap.com/kb/how-to-install-rpm-file-centos-linux/

3) https://access.redhat.com/solutions/1189/



