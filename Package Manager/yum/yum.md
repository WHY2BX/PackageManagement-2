#YUM (Yellowdog Updater Modified)
##YUM คืออะไรกันแน่?
Yellowdog Updater Modified หรือที่รู้จักกันในชื่อย่อว่า **_YUM_** เป็นเครื่องมือในการจัดการแพ็คเกจทั้งการติดตั้ง อัพเดต ลบ นิยมใช้ใน Red-Hat-based distros อย่างเช่นพวก CentOS, RHEL, OpenSUSE, Fedora, Rocky Linux. YUM จะแก้ปัญหา dependencies โดยอัตโนมัติ และจะทำการ obsolete processing โดยขึ้นอยู่กับ repository metadata ที่มีอยู่ในระบบ
นอกจากนี้ YUM ยังสามารถจัดการกับแพ็คเกจที่มีอยู่แล้วในระบบ หรือจากแพ็คเกจ **.rpm** ก็ได้ โดยที่ตัวเอกสารกำหนดค่าหลักของ YUM นั้นจะอยู่ที่ **/etc/yum.conf** รวมถึงrepositories ทุกตัวของ YUM ก็จะอยู่ที่่ **/etc/yum.repos.d**

โดยการใช้ตำสั่ง YUM ได้นั้นจะต้องเปลี่ยนเป็น root ก่อน หรือไม่ก็ใช้ sudo โดยที่ yum จะมี syntax โดยทั่วไปดังนี้

```$ sudo yum [options] [command] [package_name]```

การติดตั้งแพ็คเกจผ่าน YUM สามารถทำได้โดยการใช้คำสั่งต่อไปนี้
```$ sudo yum install [package_name]```

ตัวอย่างผลลัพธ์

```[deepak@localhost ~]$ sudo yum install iotop
...
Resolving Dependencies
--> Running transaction check
---> Package iotop.noarch 0:0.6-4.el7 will be installed
--> Finished Dependency Resolution

...
Installed:
  iotop.noarch 0:0.6-4.el7                                                                                      

Complete!```

ในส่วนของการอัพเดตแพ็คเกจผ่าน YUM สามารถใช้คำสั่งนี้

```$ sudo yum update [package_name]```

ตัวอย่างผลลัพธ์

```[deepak@localhost ~]$ sudo yum update NetworkManager
...
Resolving Dependencies
--> Running transaction check
---> Package NetworkManager.i686 1:1.18.8-1.el7 will be updated
--> Processing Dependency: NetworkManager = 1:1.18.8-1.el7 for package: 1:NetworkManager-ppp-1.18.8-1.el7.i686
--> Processing Dependency: NetworkManager = 1:1.18.8-1.el7 for package: 1:NetworkManager-tui-1.18.8-1.el7.i686
--> Processing Dependency: NetworkManager(x86-32) = 1:1.18.8-1.el7 for package: 1:NetworkManager-team-1.18.8-1.el7.i686
--> Processing Dependency: NetworkManager(x86-32) = 1:1.18.8-1.el7 for package: 1:NetworkManager-adsl-1.18.8-1.el7.i686
--> Processing Dependency: NetworkManager(x86-32) = 1:1.18.8-1.el7 for package: 1:NetworkManager-ppp-1.18.8-1.el7.i686
--> Processing Dependency: NetworkManager(x86-32) = 1:1.18.8-1.el7 for package: 1:NetworkManager-wifi-1.18.8-1.el7.i686
---> Package NetworkManager.i686 1:1.18.8-2.el7_9 will be an update
--> Processing Dependency: NetworkManager-libnm(x86-32) = 1:1.18.8-2.el7_9 for package: 1:NetworkManager-1.18.8-2.el7_9.i686

...

Updated:
  NetworkManager.i686 1:1.18.8-2.el7_9                 NetworkManager-glib.i686 1:1.18.8-2.el7_9                

Dependency Updated:
  NetworkManager-adsl.i686 1:1.18.8-2.el7_9              NetworkManager-libnm.i686 1:1.18.8-2.el7_9             
  NetworkManager-ppp.i686 1:1.18.8-2.el7_9               NetworkManager-team.i686 1:1.18.8-2.el7_9              
  NetworkManager-tui.i686 1:1.18.8-2.el7_9               NetworkManager-wifi.i686 1:1.18.8-2.el7_9              

Complete!```

แต่ถ้าไม่ได้มีการระบุชื่อแพ็คเกจไว้ มันก็จะไปทำการอัพเดตแพ็คเกจทุกตัวที่ได้มีการติดตั้งไว้บนระบบ

```sudo yum update```