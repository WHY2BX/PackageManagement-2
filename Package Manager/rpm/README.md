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

# Install 
## Download RPM Files from the Internet
 * สามารถดาวน์โหลดไฟล์ RPM จากอินเทอร์เน็ตโดยใช้เว็บเบราว์เซอร์ หรือใช้คำสั่ง wget
```
wget [option] [URL]
```
### Example

## Download RPM Files from the Repository
 * สามารถใช้ yum และ dnf ช่วยให้คุณสามารถดาวน์โหลดไฟล์ RPM ได้
```
sudo yumdownloader [package_name]
```
```
dnf download [package_name]
```

การติดตั้ง rpm สามารถใช้ได้ 3 คำสั่ง คือ rpm, yum และ dnf
```
sudo rpm -i [ ชื่อ package ที่ต้องการติดตั้ง ]
```
```
sudo yum localinstall [ ชื่อ package ที่ต้องการติดตั้ง ]
```
```
sudo dnf localinstall [ ชื่อ package ที่ต้องการติดตั้ง ]
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

## Remove
ใช้ rpm
```
sudo rpm -e  [ ชื่อ package ]
```
ใช้ yum
```
sudo yum remove  [ ชื่อ package ]
```


ใช้ dnf
```
sudo dnf remove [ ชื่อ package ]
```

## Update
```
sudo rpm -Uvh [ ชื่อ package ]
```

## Verify
ใช้ตรวจสอบ package RPM ทั้งหมด
```
sudo rpm -Va
```

## Query
ค้นหาไฟล์ของ RPM package
```
rpm -qf [ ชื่อ query ]
```
ค้นหาข้อมูลของ package นั้น
```
rpm -qi [ ชื่อ query ]
```
ค้นหา document ของ package นั้น
```
rpm -qdf (query document file)
```


# reference
1) https://www.tecmint.com/20-practical-examples-of-rpm-commands-in-linux/

2) https://phoenixnap.com/kb/how-to-install-rpm-file-centos-linux/

3) https://access.redhat.com/solutions/1189/



