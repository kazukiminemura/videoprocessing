import cv2

cap = cv2.VideoCapture(0)
cap1 = cv2.VideoCapture(0)
while True:
    ret, im = cap.read()

    height = im.shape[0]
    width = im.shape[1]
    im = cv2.resize(im,(width/2, height/2))

    #blur = cv2.GaussianBlur(im, (0, 0), 5)
    tmp = cv2.Canny(im, 100, 200)
    cv2.namedWindow("tmp", cv2.WINDOW_NORMAL)
    cv2.namedWindow("img", cv2.WINDOW_NORMAL)
    cv2.imshow('tmp', tmp)
    cv2.imshow('img', im)
    key = cv2.waitKey(10)
    if key == 27:
        break

cap.release()
cv2.destroyAllWindows()
