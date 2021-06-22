# Docker Command basic
```
1
docker run {image_name} {optional_comand} => ใช้รันสร้าง docker container

ex
    docker run Ubuntu echo "hello world"

- - -(add option) - - -

docker run -it {image_name} sh   => run docker แล้วเข้า shell 

docker run --name {container_name} {image_name} => รันสร้าง docker container และกำหนดชื่อ

docker run -d {image_name}  => รันแบบ background

docker run -d -p 8080:80    => รันแบบ forward port ออกมา
```
    2
    docker ps     => แสดง container ที่กำลังรัน

    docker ps -a    => แสดง container ที่มีทั้งหมด
 ```
3 docker rm {container_name / container_id}       => ลบ container
