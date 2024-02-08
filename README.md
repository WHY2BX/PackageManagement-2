# PackageManagement-3
COMPUTER ORGANIZATION AND OPERATING SYSTEM (Chapter: Package Management, Section: 3)

## Introduction to Package Management ##
  Ubuntu มีระบบในการจัดการ Package ที่ครอบคลุมสำหรับ การติดตั้ง, อัพเกรด, กำหนดค่า รวมไปถึงการ ลบ Software นอกจากนี้ยังสามารถตรวจสอบและเข้าถึงฐานข้อมูลที่มีองค์ประกอบมากกว่า 60,000 Software packages อีกด้วย 
  

- ### Package คืออะไร ? ###
  แพ็คเกจ (package) ใน Linux ก็เปรียบเสมือน Program บน Window ซึ่งจะประกอบไปด้วย หลายๆไฟล์ที่ใช้ในการทำงาน เช่น การติดตั้งโปรแกรมในลีนุกซ์ตระกูล Debian

- ### Package Management Tools ###

  เป็นเครื่องมือที่ใช้ในการจัดการ Package ทั้งติดตั้ง และถอนการติดตั้ง มีตั้งแต่ simple command-line ไปจนถึง Interface Graphics ที่ใช้ง่ายเหมาะสำหรับมือใหม่ที่กำลังหัดใช้ Ubuntu และทำให้การติดตั้งและจัดการซอฟต์แวร์บนระบบ Linux ง่ายขึ้น
  Linux มี Package Management Tools มากมายหลายชนิด แต่ที่นิยมใช้กัน ได้แก่
  1. apt และ apt-get : เครื่องมือเหล่านี้ใช้ในระบบ Debian และ Ubuntu
  2. yum : เครื่องมือนี้ใช้ในระบบ Red Hat และ CentOS
  3. dnf (Dandified yum) เป็นเครื่องมือจัดการแพ็กเกจที่ เป็นการแทนที่ yum ที่ใช้ในระบบ Fedora
  4. zypper : เครื่องมือนี้ใช้ในระบบ openSUSE

  ซึ่ง Tools เหล่านี้ก็มีคุณสมบัติที่คล้ายคลึงกัน รวมถึงมีข้อดีและข้อเสียที่แตกต่างกันไป โดยเกณฑ์จะขึ้นอยู่กับความชอบของผู้ใช้ และระบบ Linux ที่ใช้ ทำให้ไม่มีข้อสรุปว่า Tools ไหนดีทีสุด

## Introduction to Repository Setup คืออะไร? ##
    เป็นการตั้งค่
- ### Respository คืออะไร? ###
    Respository เป็นคลัง Package เวลาเราจะติดตั้งโปรแกรมอะไร ก็ไปดาวน์โหลด Package ของโปรแกรมนั้นๆ ตาม Respository ที่มันอยู่ ซึ่งโดยปกติแล้ว พวก Respository จะอยู่บน Internet เพื่อให้เครื่องที่สามารถเชื่อมต่อ Internet ได้ สามารถ Update Software ได้อย่างสม่ำเสมอ แต่บางครั้งการ Update ผ่าน Internet อาจจะเปลือง Traffic การทำ Local Respository ก็อาจจะตอบโจทย์มากกว่า ซึ่ง Package เหล่านี้ก็มีการแบ่ง ตาม Distribution ที่ใช้ด้วย เช่น ตระกูล Redhat/Fedora/SUSE จะใช้ไฟล์ .rpm แต่ถ้าเป็นตระกูล Debian/Ubuntu ก็จะใช้ไฟล์ .deb ซึ่งไม่สามารถใช้ร่วมกันได้

## Referenecs ##
# Mainpage #
-  https://feversecure.wordpress.com/2017/10/18/วิธีใช้-apt-get-บน-linux-ฉบับง่ายๆ/#:~:text=*แพ็คเกจ%20(package)%20ใน%20Linux,สำหรับหา%20packages%20ใหม่ๆ

- https://suchart.wordpress.com/debianubuntu-package-management/

- https://bard.google.com/chat/3cc46de7841e2fc6

- https://jetsadamalaisirirat.medium.com/การทำ-local-repository-สำหรับ-redhat-centos-ece9c4545960

- https://bigta.wordpress.com/2011/04/30/installing-program-in-linux/ 

## Members ##
-
-
-
- 65070233 สหัสวรรษ วงศ์บุญธเนธ
- 65070238 น.ส.สิริมงคล ทองขวัญใจ
- 65070241 น.ส.สุพิชชา วิเศษเจริญ
