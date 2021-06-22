## Docker Utilities Command set1

```
1. docker ps
```
    2 docker rename {container_name ที่ต้องการ rename} {new_name} => rename container
```
3 docker exec -it {container_name}  => ไปเข้าที่ shell ของ docker container
```
    4 docker top {container_name}   => ดู process ที่รันอยู่ข้างใน

---

## Docker Utilities Command set2

```
1 docker stop {container_name / container_id}  => หยุด container
```
    2 docker start {container_name / container_id}  => start container
```
3  => ดู log ของ container ได้เป็น std out และ std error (ไม่ใช่ file)

docker logs {container_name / container_id}     

docker logs {container_name / container_id} -f

-f เป็นการบอกว่าให้ following ตามไปเรื่อยๆ
```

---

## Docker Utilities Command set3
```
1 docker stats => ใช้หลัง app run แล้ว ใช้แสดง resource ที่ app พีื
```
    2 docker inspect {container_name / container_id / image_name / image_id} => แสดงรายละเอียด ใช้ได้ทั้ง image และ container
```
3 docker rm -f {container_name / container_id} => ลบ docker container ทียัง run อยู่
```
    4 docker rmi {image_name / image_id}    => ลบ docker image


