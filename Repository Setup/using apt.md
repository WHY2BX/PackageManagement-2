# Repository Setup ด้วย APT
ติดตั้ง Repository ด้วยคำสั่ง `add-apt-repository` ซึ่งเป็นสคริปต์ภาษา Python ที่จะช่วยติดตั้ง Repository ลงที่ `/etc/apt/sources.list` หรือจะแยกไฟล์ที่ `/etc/apt/sources.list.d` directory ก็ได้ ซึ่งคำสั่งนี้สามารถใช้เพื่อนำ Repository ที่มีอยู่แล้วออกได้ด้วย

การจะใช้คำสั่ง `add-apt-repository` นั้น จะต้องมีแพ็กเกจ `software-properties-common` ด้วย สามารถติดตั้งได้โดย
```sudo apt update
sudo apt install software-properties-common
