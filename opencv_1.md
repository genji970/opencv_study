img \= cv2.imread('/', )

\-1, cv2.IMREAD\_COLOP : Loads a color image  
0, cv2.IMREAD\_GRAYSCALE : Loads image in grayscale mode  
1 , cv2.IMREAD\_UNCHANGED : Loads image as such including alpha channel

\#  
cv2.imshow('Image', img) \-\> cv2.imshow(window\_name , img)

cv2.waitkey(0) 

cv2.destroyAllWindows()

\# resize  
img \= cv2.resize(img, (400,400))

img \= cv2.resize(img, (0,0), fx=0.5 , fy \= 0.5) \-\> img.size에 대한 multiplying

\#rotate  
img \= cv2.rotate(img, cv2.cv2.ROTAT)치면 여러 가지 함수들이 나온다

\# 저장  
cv2.imwrite('name of file', img)  
