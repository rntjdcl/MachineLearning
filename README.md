# MachineLearning

##기본 기능
1. 기본.zip에서 1.웹캠저장.txt 안의 소스코드로 노트북 캠으로 팬을 찍어서 저장하였다.
2. 기본 zip에서 2.움직이는 물체 라벨링하고 이미지 데이터 저장.txt
3. 데이터 저장을 한 파일이 image 파일이다. 지우개는 비교를 위해서 네이버 이미지 검색에서 캡처를 했다.
4. image를 구별하기 위해서 image를 pen과 eraser로 나누어서 저장해주었다.
5. cmd 창에서 inceptionv3_retrain.p의 저장 경로로 이동하고 python inceptionv3_retrain.py --image_dir C:\\image 의 명령어를 실행해주었다.
6. 그럼 학습이 진행하는 것을 확인할 수 있다. test데이터와 학습데이터는 80/20의 비율도 무작위로 설정되어있다.
7. 학습은 구글에서 만든 inception v3모델을 활용했다.
8. 1000번의 traing step이 진행되고 학습이 완료된다.
retraining된 graph 파일의 저장경로 : /tmp/output_graph.pb
output label들의 저장경로 : /tmp/output_labels.txt
9. 잘 학습됬는지 알아보기 위해서 python retrain_run_inference.py의 명령어로 확인한다.
10. retrain_run_inference.py의 코드안에 line8에 이미지 경로를 설정하면 그 사진으로 확인을 할 수 있다.
11. 내가 분류한 이미지들로 98%이상의 정확도를 보이는 것을 알 수 있었다.

>>http://solarisailab.com/archives/1422

##심화 기능
>>http://solarisailab.com/archives/2387