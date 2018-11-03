http://solarisailab.com/deep-learning
https://ukayzm.github.io/python-object-detection-tensorflow/    동영상


개발 과제 - 머신러닝

[과제]

웹캠을 이용한 사물 및 사람 인식 프로그램

웹캠에 사물이나 얼굴을 보여준 뒤, 무엇인지 정보를 주어 학습시킨 다음, 다시 사물이나 얼굴을 보여주면 인공지능이 무엇인지 알려주는 프로그램.

 
공통 사항:

1) 필요한 기술 
웹캠 연동 : Python, OpenCV
데이터셋 제작 툴 : Python, OpenCV
모델 개발 및 학습 : Keras

2) 상세 시나리오
1.웹캠에 사물이나 사람 얼굴을 보여주면서 동영상 파일로 저장한다.
2.저장된 동영상을 읽어서 특정 프레임을 선택하여 라벨링을 수행한다. (여기서 라벨링이란 특정 사물이나 사람을 지정하는 행위)
3.특정 프레임과 라벨링 정보를 이용하여 데이터셋을 생성한다.
4.이미지 분류에 적합한 모델을 개발한다.
5.생성된 데이터셋을 개발한 모델에 학습시킨다.
6.웹캠에 들어오는 영상을 학습시킨 모델에 입력하여 모델 결과를 화면에 출력한다.

[기본버전]

위 내용을 구현하되, 단순히 분류만 한다.
라벨링은 프레임 이미지 단위로 한다.
CNN 등 분류 모델 사용

[가산점]

객체 검출 즉 객체에 위치(사각형)을 표시하고 그 객체가 무엇인지 표시한다.
라벨링은 프레임 이미지별 객체 위치(사각형, bounding box)를 표시한다.
Object Dectection에 사용하는 yolo, ssd, 등 사용

[제출물]

과제를 완료한 Github주소를 메일로 제출

readme에 구동방법을 자세히 안내


python inceptionv3_retrain.py --image_dir C:\\cat_photos 
python retrain_run_inference.py 