# NewLearn 알고리즘

이 디렉토리에는 Ultralytics LLC에서 개발한 YOLOv5 소프트웨어가 포함되어 있으며 GPL-3.0 라이선스에 따라 무료로 재배포할 수 있습니다. 자세한 내용은 https://github.com/ultralytics/yolov5 참조하세요.

## YOLOv5

### 1)설치

```bash
pip install -r requirements.txt
```

### 2)데이터셋 준비

1. [Newlearn](https://newlearn.ai/)에서 데이터 업로드, 전처리, 라벨링을 진행하고 데이터 세트를 다운을 진행
2. 훈련 데이터세트 중 이미지는 data/train/images, 라벨데이터는 daya/train/labels에 복사
3. 테스트 데이터세트 중 이미지는 data/test/images, 라벨데이터는 daya/test/labels에 복사
4. data/data.yaml 훈련과 검증 데이터 경로와 훈련하고자 하는 라벨을 설정, nc는 라벨개수 +1로 설정, names의 마지막 값은 NA로 설정

```bash
train:  data/train
val: data/test
nc: 2
names: [CAR, NA]
```

### 2)훈련

1. train.py 실행

```bash
python train.py --epoch 100 --batch-size 4 --learning-rate 0.001 --algorithm yolov5
```

### 3)검증

1. detect.py 카메라 검증

```bash
python detect.py --weights data/yolov5s.pt --source 0
```

2. detect.py 비디오 검증

```bash
python detect.py --weights data/yolov5s.pt --source test.mp4 --view-img
```
