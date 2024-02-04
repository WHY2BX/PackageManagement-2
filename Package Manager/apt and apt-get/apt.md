#APT(Advanced Package Tool)

##อะไร คือ APT package manager
เป็นเครื่องมือสำหรับการจัดการ package ของ Linux ในตระกูล Dabian จึงรวมไปถึง Ubuntu ด้วยเช่นกัน


##คำสั่งต่างๆ


###Install

Install package เดียว
apt install ชื่อpackage

Install หลาย package 
apt install <ชื่อpackage เเรก> <ชื่อpackage สอง>



###Uninstall

apt remove ชื่อpackage
ลบ package ที่ไม่ได้ทำการลบการ data files เเละ configuration file

apt purge ชื่อpackage 
ลบ package ที่ทำการลบการ data files เเละ configuration file ของไฟล์ออกไปด้วย

apt autoremove
ลบ ส่วนที่เป็น dependency ของ package ที่ถูกไปเเล้วเเต่ยังค้างอยู่ในระบบทั้งหมด

apt autoremove ชื่อpackage
ลบเฉพาะ dependency ของ  pacakage ที่ระบุ

###Reinstall
reinstall ชื่อ package

###Upgrade Package
apt update
ก่อนที่จะทำการ upgrade เราควรใช้คำสั่ง update เพื่อดึงข้อมูล version ล่าสุดของ package นั้นๆ

apt upgrade
apt สามารถใช้คำสั่งนี้คำสั่งเดียวเพื่อ upgrade package ทั้งหมดที่เราติดตั้งเอาไว้

apt upgrade ชื่อ package
สำหรับ upgrade เฉพาะ package ที่ต้องการ

###Search
apt search ชื่อpackage
หา package ที่เราต้องการ output จะเป็น list ของ package ที่ตรงกับ input ของเรา ทำให้เราหา package ที่เราต้องการได้ง่ายขึ้น 


##การจัดการ repository ด้วย apt


#reference
1)https://blog.packagecloud.io/what-is-the-apt-package-manager-why-and-how-to-use-it/
2)https://contabo.com/blog/managing-packages-with-the-apt-package-manager/




