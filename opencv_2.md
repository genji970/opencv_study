cap \= cv2.VideoCapture(0) 0: webcam

cap \= cv2.VideoCapture('file\_name')

while True:  
    ret , frame \= cap.read()  
    \# ret : 잘 가져왔으면 True , 못 가져왔거나 비디오의 끝이면 False  
    \#frame : 한 프레임

    width \= int(cap.get(3)) \# cap.get에는 cv.\~로 프레임수, 높이,너비 등을 가져올수있는데 특정 숫자가 인덱싱되어있다  
    height \= int(cap.get(4))

    image \= np.zeros(frame.shape , np.uint8)  
    smaller\_frame \= cv2.resize(frame, (0,0), fx=0.5, fy=0.5)  
    \# (0,0)은 명시적인 height,width를 제공하지 않겠다는 의미다

    cv2.imshow('frame', frame)

    if cv2.waitKey(1) \== ord('q'):  
        break

    cap.release()  
    cv2.destroyAllWindows()  
