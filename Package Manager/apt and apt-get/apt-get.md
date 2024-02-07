# apt-get

## อะไร คือ apt-get package manager
apt-get เป็น tool ที่ช่วยจัดการ package ใน Debian-based Linux เช่น Ubuntu หน้าที่หลักคือการดึงข้อมูล เเละ package จากแหล่งที่มาที่น่าเชื่อถือ 
เพื่อทำการ ติดตั้ง(install),อัพเกรด(upgrade), ลบ(removal) package รวมถึง dependency ของ package

## คำสั่งต่างๆ

### Install
```
apt-get install ชื่อpackage
Example
apt-get install vim nano mc
```
ติดตั้ง package 1อันหรือมากกว่า
```
apt-get install –reinstall ชื่อpackage
```
ถ้าหากมี package อยู่เเล้วเเต่ต้องการที่จะย้อนกลับไปเป็น default state สามารถใช้คำสั่งนี้ได้


### Uninstall
```
apt-get remove ชื่อpackage
```
คำสั่งสำหรับถอนการติดตั้ง package ที่ต้องการ
```
apt-get purge [package_name]
```
คำสั่งสำหรับถอนการติดตั้ง package เช่นเดียวกันเเต่จะทำการลบ configuration file ของ package ออกไปด้วย
### Upgrade
```
apt-get update
```
ใช้เพื่อ update package ทั้งหมดที่ผู้ใช้ติดตั้ง เพื่อให้ระบบรู้ว่ามีเวอร์ชันล่าสุดของ package อยู่เป็นการเตรียมการก่อนการใช้ upgrade
```
apt-get upgrade
```
ใช้เพื่อติดตั้งเวอร์ชันล่าสุดของ package ที่ผู้ใช้ติดตั้ง โดยต้องทำการ update ก่อนการ upgrade

dselect-upgrade	
dist-upgrade

### คำสั่งอื่นๆ
```
apt-get check
```
ใช้เพื่อทำการตรวจสอบว่ามี package ที่เกิดความเสียหายหรือไม่
```
apt-get clean
```
ใช้เพื่อลบ files cache ของ package
```
apt-get show
```
ใช้เพื่อเสดงข้อมูลของ package เช่น เวอร์ชัน, คำอธิบายของ package 
```
apt-get list
Ex
sudo apt-get list --installed
จะเเสดง list ของ package ที่ผู้ใช้ติดตั้งเอาไว้
```
แสดง listของ package ตามเงื่อนไขที่เรากำหนด

# reference
1)https://www.geeksforgeeks.org/apt-get-command-in-linux-with-examples/
