# NewLearn 알고리즘

# YOLOv5

## 1)설치

```bash
pip install -r requirements.txt
```

## 2)데이터셋 준비

1. 훈련, 검증 데이터세트 분할
2. 훈련 데이터세트 중 이미지는 data/train/images, 라벨데이터는 daya/train/labels에 복사
3. data.yaml 훈련과 검증 데이터 경로와 훈련하고자 하는 라벨을 설정, nc는 라벨개수 +1로 설정, names의 마지막 값은 NA로 설정

```bash
train: ./data/train
val: ./daya/test
nc: 2
names: [CAR, NA]
```

## 2)훈련

1. train.py 실행

```bash
python train.py --epoch 100 --batch-size 4 --learning-rate 0.001
```

# NewLearn에서 데이터 세트 준비

[Newlearn](https://newlearn.ai/)는 컴퓨터 비전을 위한 데이터 세트의 관리, 전처리, 증강 및 버전 관리를 원활하게 만듭니다.  
Newlearn에서 보다 쉽게 데이터 업로드, 전처리, 라벨링을 보다 쉽게 진행 할 수 있습니다.

![logo](https://user-images.githubusercontent.com/77031838/191424048-14ed0a19-ab49-4e9c-b0ee-f2f9ada93f52.png)
