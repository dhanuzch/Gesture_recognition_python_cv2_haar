import numpy as np
import cv2
from time import sleep



lpalm_cascade = cv2.CascadeClassifier('lpalm.xml')
left_cascade = cv2.CascadeClassifier('left.xml')
fist_cascade = cv2.CascadeClassifier('fist.xml')
right_cascade = cv2.CascadeClassifier('right.xml')
rpalm_cascade = cv2.CascadeClassifier('rpalm.xml')  



cap = cv2.VideoCapture(0)

while 1:
    ret, img = cap.read()
    
    
    #gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
    
    
    lpalm = lpalm_cascade.detectMultiScale(img, 1.1, 3)
    left = left_cascade.detectMultiScale(img, 1.1, 3)
    fist = fist_cascade.detectMultiScale(img, 1.1, 3)
    right = right_cascade.detectMultiScale(img, 1.1, 3)
    rpalm = rpalm_cascade.detectMultiScale(img, 1.1, 3)
    
    
    
    
    for (x,y,w,h) in lpalm:
        font = cv2.FONT_HERSHEY_SIMPLEX
        cv2.putText(img,'Left palm',(x-w,y-h), font, 0.5, (11,255,255), 2, cv2.LINE_AA)
        sleep(1)
         

    for (x,y,w,h) in left:
        font = cv2.FONT_HERSHEY_SIMPLEX
        cv2.putText(img,'Left Hand',(x-w,y-h), font, 0.5, (11,255,255), 2, cv2.LINE_AA)
        sleep(1)
             
        
    for (x,y,w,h) in fist:
        font = cv2.FONT_HERSHEY_SIMPLEX
        cv2.putText(img,'Fist',(x-w,y-h), font, 0.5, (11,255,255), 2, cv2.LINE_AA)        
        sleep(1)
               
        
    for (x,y,w,h) in right:
        font = cv2.FONT_HERSHEY_SIMPLEX
        cv2.putText(img,'Right Hand',(x-w,y-h), font, 0.5, (11,255,255), 2, cv2.LINE_AA)   
        sleep(1)
               
        
    for (x,y,w,h) in rpalm:
        font = cv2.FONT_HERSHEY_SIMPLEX
        cv2.putText(img,'Right Palm',(x-w,y-h), font, 0.5, (11,255,255), 2, cv2.LINE_AA)       
        sleep(1)
       

    cv2.imshow('img',img)
    k = cv2.waitKey(30) & 0xff
    if k == 27:
        break

cap.release()
cv2.destroyAllWindows()
