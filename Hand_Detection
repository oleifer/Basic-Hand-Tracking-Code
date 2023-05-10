# Hand Tracking Basic code

# import libraries
# cvzone uses Mediapipe so need to have it in the system
import cv2 
from cvzone.HandTrackingModule import HandDetector

# get camera feed, choose camera device
cap = cv2.VideoCapture(0)

# Hand detector
detector = HandDetector(detectionCon=0.8, maxHands=1, minTrackCon=0.5)

while cap.isOpened():

    # detect feed
    not_needed, frame = cap.read()
    
    # find hand landmarks
    hands, frame = detector.findHands(frame)

    # show frame
    cv2.imshow('Window Name', frame)

    # quit with q
    if cv2.waitKey(10) & 0xFF == ord('q'):
        break

    # quit with the close window button
    if cv2.getWindowProperty('Window Name', cv2.WND_PROP_VISIBLE) < 1:
        break

# close all windows
cap.release() 
cv2.destroyAllWindows() 
