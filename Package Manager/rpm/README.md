# RPM (Red Hat Package Manager)
## RPM คืออะไร 
RPM (Red Hat Package Manager) เป็น default open source และเป็น utility ใน package management ที่ค่อนข้างได้รับความนิยมสำหรับคนที่ใช้ Red Hat (ex. RHEL, CentOS และ Fedora) โดย RPM เป็นเครื่องมือที่ช่วยทำให้ผู้ใช้งาน หรือผู้ดูแลระบบสามารถทำการ install, update, uninstall, query, verify รวมไปถึงจัดการ package ในระบบปฏิบัติการ Unix/Linux ได้

## Command พื้นฐาน
*Install : ใช้สำหรับติดตั้งแพ็คเกจ RPM\
*Remove : ใช้เพื่อลบ หรือยกเลิกการติดตั้งแพ็คเกจ RPM\
*Update : ใช้เพื่ออัปเดตแพ็คเกจ RPM ที่มีอยู่\
*Verify : ใช้เพื่อตรวจสอบแพ็คเกจ RPM\
*Query : ใช้ในการสืบค้นแพ็คเกจ RPM

## การ Check dependencies ก่อนติดตั้ง RPM
การตรวจ dependencies ก่อนติดตั้งจะช่วยป้องกันปัญหาที่อาจเกิดขึ้นในกระบวนการติดตั้งหรือในการใช้งานแพ็คเกจนั้น ๆ ในภายหลังได้
```
sudo rpm -qpR [ ชื่อpackage ]
```
  *q - บอกให้ RPM ทำการค้นหาแพ็คเกจ\
  *p – ระบุแพ็คเกจเป้าหมายที่จะค้นหา\
  *R – นี่แสดง requirements สำหรับแพ็คเกจ

