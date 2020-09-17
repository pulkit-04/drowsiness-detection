# drowsiness-detection
An application to find if a driver or person is feeling sleepy and give an alarm to him/her up



## You will need the code file drowsiness.py
1. A sound,alarm file (.wav)
2. A shape_predictor_68_face_landmarks.dat file that to used to landmark 62 points on face at fix location through which python can get certain region of face

## You need to pip install following modules
1. scipy
2. imutils
3. threading
4. numpy
5. playsound
6. time
7. dlib
8. cv2

## Algorithm
Each eye is represented by 6 (x, y)-coordinates, starting at the left-corner of the eye (as if you were looking at the person), and then working clockwise around the eye:.

With these points we find eye aspect ratio(ear) of each eye and take an average:.

vertically distance.
A = dist.euclidean(eye[1], eye[5]).
B = dist.euclidean(eye[2], eye[4]).
horizontally distance.
C = dist.euclidean(eye[0], eye[3]).


## formula
ear = (A + B) / (2.0 * C).

similarly we will find ear for other eye.
