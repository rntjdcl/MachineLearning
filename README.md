# MachineLearning

##�⺻ ���
1. �⺻.zip���� 1.��ķ����.txt ���� �ҽ��ڵ�� ��Ʈ�� ķ���� ���� �� �����Ͽ���.
2. �⺻ zip���� 2.�����̴� ��ü �󺧸��ϰ� �̹��� ������ ����.txt
3. ������ ������ �� ������ image �����̴�. ���찳�� �񱳸� ���ؼ� ���̹� �̹��� �˻����� ĸó�� �ߴ�.
4. image�� �����ϱ� ���ؼ� image�� pen�� eraser�� ����� �������־���.
5. cmd â���� inceptionv3_retrain.p�� ���� ��η� �̵��ϰ� python inceptionv3_retrain.py --image_dir C:\\image �� ��ɾ �������־���.
6. �׷� �н��� �����ϴ� ���� Ȯ���� �� �ִ�. test�����Ϳ� �н������ʹ� 80/20�� ������ �������� �����Ǿ��ִ�.
7. �н��� ���ۿ��� ���� inception v3���� Ȱ���ߴ�.
8. 1000���� traing step�� ����ǰ� �н��� �Ϸ�ȴ�.
retraining�� graph ������ ������ : /tmp/output_graph.pb
output label���� ������ : /tmp/output_labels.txt
9. �� �н������ �˾ƺ��� ���ؼ� python retrain_run_inference.py�� ��ɾ�� Ȯ���Ѵ�.
10. retrain_run_inference.py�� �ڵ�ȿ� line8�� �̹��� ��θ� �����ϸ� �� �������� Ȯ���� �� �� �ִ�.
11. ���� �з��� �̹������ 98%�̻��� ��Ȯ���� ���̴� ���� �� �� �־���.

>>http://solarisailab.com/archives/1422

##��ȭ ���
>>http://solarisailab.com/archives/2387