# MachineLearning

##기본 기능
1. 웹캠저장.py 안의 소스코드로 노트북 캠으로 팬을 찍어서 저장하였다.
2. 움직이는물체라벨링.py
3. 가만히 있는 물체를 수동이외에 소스코드로 만은 감지하기 힘들기 때문에 움직이는 물체라는 기준을 두고 실행했다.
4. 데이터 저장을 한 파일이 image 파일이다. 지우개는 비교를 위해서 네이버 이미지 검색에서 캡처를 했다.
5. image를 구별하기 위해서 image를 pen과 eraser로 나누어서 저장해주었다.
6. cmd 창에서 inceptionv3_retrain.p의 저장 경로로 이동하고 python inceptionv3_retrain.py --image_dir C:\\image 의 명령어를 실행해주었다.
7. 그럼 학습이 진행하는 것을 확인할 수 있다. test데이터와 학습데이터는 80/20의 비율도 무작위로 설정되어있다.
8. 학습은 구글에서 만든 inception v3모델을 활용했다.
9. 1000번의 traing step이 진행되고 학습이 완료된다.
retraining된 graph 파일의 저장경로 : /tmp/output_graph.pb
output label들의 저장경로 : /tmp/output_labels.txt
10. 잘 학습됬는지 알아보기 위해서 python retrain_run_inference.py의 명령어로 확인한다.
11. retrain_run_inference.py의 코드안에 line8에 이미지 경로를 설정하면 그 사진으로 확인을 할 수 있다.
12. 내가 분류한 이미지들로 98%이상의 정확도를 보이는 것을 알 수 있었다.

>>http://solarisailab.com/archives/1422

##심화 기능

심화기능은 object_detection ssd를 활용해서 위에서 학습한 사진들로만 확인만 해보았습니다.
지우개의 경우에는 책으로 판별을 했고, 팬의 경우에는 판별을 하지못했습니다. (지우개.jpg)
그리고 대표적으로 주어진 사진 2개가 있었는데, 그것들은 잘 판별되는 것을 확인했습니다.(대표1.jpg,대표2.jpg)
>>http://solarisailab.com/archives/2387