# Docker Roles

Roles
- Image
- Container
- Engine
- Registry

## Docker Image
ลักษณะการทำงานเป็น layer (Read only)

Inside docker image

1.Base OS (linux os such as Ubuntu, Alpine)

2.System Package (APT)

3.Library dependencies (pip/npm ขึ้นอยู่กับ app)

4.Configuration

5.Source code

โดยเขียนเป็น docker file (พูดง่ายๆคือ docker image เกิดจาก docker file)

---

## Docker file

เป็น instrcution code


    FROM {OS + System Package}

    COPY {path sourcecode} {path in docker}

    WORKDIR {place that app exist}

    RUN {cmd library dependencies}

    ENV {configuration}

    EXPOSE {port to access docker}

    CMD {order array of cmd}

---

## Docker Container 

เป็นตัวที่เกิดจากการ build docker image (Read, Write layer)

ประกอบด้วย 2 ตัวใหญ่ๆ
1 process
2 write file

มองง่ายๆ docker image เป็น class , ส่วน docker container เป็น instance ของ class -> แปลว่าเราสามารถสร้าง container ได้หลาย container จาก image เดียว

---

## Docker Engine

เป็น process ที่ run ดูแล docker image และ docker cotainer ในระบบ (เช่นเราสั่ง cli docker จริงๆแล้วมันคือการสั่งเข้าไปที่ docker engine)

---

## Docker Registry

เป็นที่ที่เก็บ docker image 

ที่ๆแรกที่ docker image จะถูกเก็บคือในเครื่อง host ที่ได้สร้าง docker image ขึ้นมา และยังสามารถเก็บได้ที่อื่่นอีก คือ 1.public และ 2. private

1. Public => เป็นตัว docker hub

2. Pravate => ถูกเก็บไว้ที่ server ของ organize นั้นๆ

