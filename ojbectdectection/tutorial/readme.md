# Obeject Detection 

### 1. Yolo_mark 실행 

- yolo_mark directory에서 


```
cmake .
make
./linux_mark.sh
```

 ### 2. Training image 넣기 
 
 - Training 시킬 Data set을 아래의 디렉토리에 넣는다.  
 
 yolo_mark/x64/Release/data/img 에서 원하는 image로 넣는다. 

### 3. classificatin classes setting 
yolo_mark/x64/Release/data  경로에서 

`gedit obj.data` 

4. class의 이름 setting 

```yolo_mark/x64/Release/data  -경로에서

vi obj.names```

5. Boxting 

yolo_mark 

./linux_mark.sh


# 5. Start traing using the Deep learning model

## 5.1 
아래의 디렉토리에서 
yolo_mark/x64/Release 

gedit yolo-obj.cfg

Region 설정 ( classes ) 

filter 계산 equation 

$$ 5 * (classes + 5 ) $$ 


## 5.2

- yolo-obj.cfg파일도 darknet 디렉토리로 이동

- yolo_mark/x64/Release/data 경로안에 있는 image 디렉토리와 obj.names , obj.data , train.txt를 darknet/data 경로로 이동



## 5.3 

Starting traing 

cd darknet

./darknet detector train data/obj.data yolo-obj.cfg darknet19_448.conv.23


## 5.4 traing 되면서 weights 생성 및 로그 

ex  ) yolo 100 .weights.... 

# 6. 

Detect with Webcam using the weight 

- image 

./darknet detector test data/obj.data yolo-obj.cfg backup/yolo-obj_10000.weights data/<image file>

- video

./darknet detector demo data/obj.data yolo-obj.cfg backup/yolo-obj_10000.weights data/<video file>


- Webcam


./darknet detector demo data/obj.data yolo-obj.cfg backup/yolo-obj_10000.weights data



