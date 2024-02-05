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

### Reinstall
```
reinstall ชื่อ package
```
คำสั่งนี้คืิอการลง packge นั้นใหม่อีกครั้งหลังจากลบทิ้งไป หรือ หากเกิดความเสียหายกับ package ก็สามารถใช้คำสั่งนี้ได้เช่นกัน (3)

### Upgrade Package
```
apt update
```
ก่อนที่จะทำการ upgrade เราควรใช้คำสั่ง update เพื่อดึงข้อมูล version ล่าสุดของ package นั้นๆมาก่อน

```
apt upgrade
```
apt สามารถใช้คำสั่งนี้คำสั่งเดียวเพื่อ upgrade package ทั้งหมดที่เราติดตั้งเอาไว้

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
จะได้ output เป็น ข้อมูลของ package ดังนี้ (3) <br>
-Package: ชื่อของ package <br>
-Version: version ของ package <br>
-Installed-Size: จำนวนพื้นที่ที่ package นั้นใช้บน disk โดยไม่ได้รวมถึง dependency ของ package <br>
-Depends: list ของ dependency <br>
-APT-Manual-Installed: Designates if the package was manually installed or automatically installed (for instance, like as a dependency for another package). This is visible within apt (not apt-cache). <br>
-APT-Sources: The repository where the package information was stored. This is visible within apt (not apt-cache). <br>
-Description: คำอธิบายของ package


## การจัดการ repository ด้วย apt
--ยังไม่เสร็จ--
A repository is a collection of packages (typically for a specific Linux distribution and version) that are stored on a remote system. This enables software distributors to store a package (including new versions) in one place and enable users to quickly install that package onto their system. In most cases, we obtain packages from a repository - as opposed to manually downloading package files.

Information about repositories that are configured on your system are stored within /etc/apt/sources.list or the directory /etc/apt/sources.list.d/. Repositories can be added manually by editing (or adding) a sources.list configuration file, though most repositories also require adding the GPG public key to APT’s keyring. To automate this process, it’s recommended to use the add-apt-repository utility.

### การเพิ่ม repository
```
 add-apt-repository urlของrepository
```
### การลบ repository
```
 add-apt-repository --remove urlของrepository
```

##


# reference
1)https://blog.packagecloud.io/what-is-the-apt-package-manager-why-and-how-to-use-it/

2)https://contabo.com/blog/managing-packages-with-the-apt-package-manager/

3)https://www.linode.com/docs/guides/apt-package-manager/




