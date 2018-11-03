import cv2 as cv
cap = cv.VideoCapture(0)
fourcc = cv.VideoWriter_fourcc(*'XVID')
out = cv.VideoWriter('test7.avi',fourcc, 20.0, (640,480))
while(cap.isOpened()):
    ret, frame = cap.read()
    out.write(frame)
    cv.imshow('frame',frame)
    if cv.waitKey(1) & 0xFF == ord('q'):
        break
cap.release()
out.release()
