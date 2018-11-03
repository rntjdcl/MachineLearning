#https://docs.opencv.org/3.4.3/db/d5c/tutorial_py_bg_subtraction.html

import cv2
import numpy as np

cap = cv2.VideoCapture("test.avi")
fgbg = cv2.createBackgroundSubtractorMOG2(history=500, varThreshold=500, detectShadows=0)
count = 0

while(1):
    count = count + 1
    ret, frame = cap.read()

    width = frame.shape[1]
    height = frame.shape[0]
    frame = cv2.resize(frame, (int(width*0.5), int(height*0.5)))
    fgmask = fgbg.apply(frame)

    nlabels, labels, stats, centroids = cv2.connectedComponentsWithStats(fgmask)

    count2 =0
    for index, centroid in enumerate(centroids):
        count2 = count2+1
        if stats[index][0] == 0 and stats[index][1] == 0:
            continue
        if np.any(np.isnan(centroid)):
            continue


        x, y, width, height, area = stats[index]
        centerX, centerY = int(centroid[0]), int(centroid[1])

        if area > 2000 and count >100:
            img_trim = cv2.rectangle(frame, (x-30, y-30), (x + width+30, y + height+30), (0, 0, 255))
            img_trim = frame[y - 30:y + height + 30, x - 30:x + width + 30]
            cv2.imwrite("C:/Users\Babo/PycharmProjects/MachineLearning/test_image/freame%d_%d.jpg" % (count, count2), img_trim)

    cv2.imshow('mask',fgmask)
    cv2.imshow('frame',frame)

    k = cv2.waitKey(30) & 0xff
    if k == 27:
        break

cap.release()
cv2.destroyAllWindows()