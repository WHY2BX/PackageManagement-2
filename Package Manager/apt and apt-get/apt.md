# APT(Advanced Package Tool)

## อะไร คือ APT package manager
เป็นเครื่องมือสำหรับการจัดการ package ของ Linux ในตระกูล Dabian จึงรวมไปถึง Ubuntu ด้วยเช่นกัน


## คำสั่งต่างๆ


### Install


```
apt install ชื่อpackage
```
Install package เดียว

```
apt install <ชื่อpackage เเรก> <ชื่อpackage สอง>
```
Install หลาย package 

```
reinstall ชื่อ package
```
คำสั่งนี้คืิอการลง packge นั้นใหม่อีกครั้งหลังจากลบทิ้งไป หรือ หากเกิดความเสียหายกับ package ก็สามารถใช้คำสั่งนี้ได้เช่นกัน `(3)`
```
apt list --installed
```
เเสดง list ของ package ที่เรา install เอาไว้




### Uninstall
```
apt remove ชื่อpackage
```
ลบ package ซึ่งจะไม่ทำการลบการ data files เเละ configuration file

```
apt purge ชื่อpackage
```
ลบ package ซึ่งจะทำการลบ data files เเละ configuration file ออกไปด้วย

```
apt autoremove
```
ลบ ส่วนที่เป็น dependency ของ package ที่ถูกไปเเล้วเเต่ยังค้างอยู่ในระบบทั้งหมด

```
apt autoremove ชื่อpackage
```
ลบเฉพาะ dependency ของ  pacakage ที่ระบุ


### Upgrade
```
apt update
```
ก่อนที่จะทำการ upgrade เราควรใช้คำสั่ง update เพื่อดึงข้อมูล version ล่าสุดของ package มาก่อน

```
apt upgrade
```
คำสั่งนี้จะทำการทำให้ package อยู่ในเวอร์ชันล่าสุดของมันเพื่อเพิ่มศักยภาพการทำงานเเละเพิ่มความปลอดภัยของpackage apt สามารถใช้คำสั่งนี้คำสั่งเดียวเพื่อ upgrade package ทั้งหมดที่เราติดตั้งเอาไว้

```
apt upgrade ชื่อpackage
```
สำหรับ upgrade เฉพาะ package ที่ต้องการ
```
apt list --upgradable 
```
คำสั่งเเสดง list ของ package ที่เราสามารถ update ได้


### Search
```
apt search ชื่อpackage
```
หา package ที่เราต้องการ output จะเป็น list ของ package ที่ตรงกับ input ของเรา ทำให้เราหา package ที่เราต้องการได้ง่ายขึ้น 

### เเสดงข้อมูลของ package 
```
apt show ชื่อpackage
```
จะได้ output เป็น ข้อมูลของ package ดังนี้ `(3)` <br>
-Package: ชื่อของ package <br>
-Version: version ของ package <br>
-Installed-Size: จำนวนพื้นที่ที่ package นั้นใช้บน disk โดยไม่ได้รวมถึง dependency ของ package <br>
-Depends: list ของ dependency <br>
-APT-Manual-Installed: ระบุว่า package นั้นถูก install เเบบ manul หรือ install เเบบอัตโนมัติ <br>
-APT-Sources: repository ที่เก็บข้อมูลของ package นั้นๆ <br>
-Description: คำอธิบายของ package

## อะไรคือความเเตกต่างระหว่าง apt เเละ apt-get

1.apt เป็น เวอร์ชันใหม่กว่าของ apt-get  โดย apt-get ถูกปล่อย 1998 ตามมาด้วย apt ที่ถูกปล่อยในปี 2014 <br>
2.คำสั่งของ apt ถูกสร้างขึ้นมาให้มีความใช่ง่ายกว่า apt-get รวมถึง interface ของ apt ที่เป็น high-level UI จึงใช้งานง่ายกว่า apt-get ที่เป็น low-level UI <br>
3.apt สามารถใช้คำสั่ง apt search ชื่อpackage เพื่อค้นหา package ในขณะที่ apt get นั้นไม่สามารถทำได้จึงอาจจะต้องไปพึ่งพา apt-cache เเทน


## การจัดการ repository ด้วย apt `(3)`
--ยังไม่เสร็จ--


repository คือ เเหล่งรวม package ซึ่งเปิดให้ ผู้จัดจำหน่าย software(software distributor) เก็บ package ในที่ๆเดียว ซึ่งทำให้ ผู้ใช้งานสามารถ install package นั้น บนระบบของตัวเองได้อย่างรวดเร็ว ซึ่งโดยปกติเราก็มักจะ install package จาก repository มากกว่าลงเเบบ manual จาก package file ตรงๆอยู่เเล้ว 


ข้อมูลเกี่ยวกับการตั้งค่าของ repository มักจะถูกเก็บบน directory  /etc/apt/sources.list หรือ /etc/apt/sources.list.d/.
### การเพิ่ม repository
```
 add-apt-repository urlของrepository
```
### การลบ repository
```
 add-apt-repository --remove urlของrepository
```




# reference
1)https://blog.packagecloud.io/what-is-the-apt-package-manager-why-and-how-to-use-it/

2)https://contabo.com/blog/managing-packages-with-the-apt-package-manager/

3)https://www.linode.com/docs/guides/apt-package-manager/

4)https://aws.amazon.com/compare/the-difference-between-apt-and-apt-get/



