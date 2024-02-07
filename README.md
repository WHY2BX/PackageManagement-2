# PackageManagement-3
COMPUTER ORGANIZATION AND OPERATING SYSTEM (Chapter: Package Management, Section: 3)

## Introduction to Package Management ##
  Ubuntu มีระบบในการจัดการ Package ที่ครอบคลุมสำหรับ การติดตั้ง, อัพเกรด, กำหนดค่า รวมไปถึงการ ลบ Software นอกจากนี้ยังสามารถตรวจสอบและเข้าถึงฐานข้อมูลที่มีองค์ประกอบมากกว่า 60,000 Software packages อีกด้วย 
  

### Package คืออะไร ? ###
  แพ็คเกจ (package) ใน Linux ก็เปรียบเสมือน Program บน Window ซึ่งจะประกอบไปด้วย หลายๆไฟล์ที่ใช้ในการทำงาน เช่น การติดตั้งโปรแกรมในลีนุกซ์ตระกูล Debian

### Package Management Tools ###

  เป็นเครื่องมือที่ใช้ในการจัดการ Package ทั้งติดตั้ง และถอนการติดตั้ง มีตั้งแต่ simple command-line ไปจนถึง Interface Graphics ที่ใช้ง่ายสำหรับ มือใหม่ที่กำลังหัดใช้ Ubuntu และทำให้การติดตั้งและจัดการซอฟต์แวร์บนระบบ Linux ง่ายขึ้นโดยไม่ต้องคอมไพล์ซอฟต์แวร์จากต้นทาง
  Linux มี Package Management Tools มากมายหลายชนิด แต่ที่นิยมใช้กัน ได้แก่
  1. apt และ apt-get : เครื่องมือเหล่านี้ใช้ในระบบ Debian และ Ubuntu
  2. yum : เครื่องมือนี้ใช้ในระบบ Red Hat และ CentOS
  3. dnf (Dandified yum) เป็นเครื่องมือจัดการแพ็กเกจที่ เป็นการแทนที่ yum ที่ใช้ในระบบ Fedora
  4. zypper : เครื่องมือนี้ใช้ในระบบ openSUSE

  ซึ่ง Tools เหล่านี้ก็มีคุณสมบัติที่คล้ายคลึงกัน รวมถึงมีข้อดีและข้อเสียที่แตกต่างกันไป โดยเกณฑ์จะขึ้นอยู่กับความชอบของผู้ใช้ และระบบ Linux ที่ใช้ ทำให้ไม่มีข้อสรุปว่า Tools ไหนดีทีสุด

  ## Repository Setup คืออะไร? ##
    เป็นการตั้งค่า
