# Face-Detection-Using-Deep-Learning

Face detection, also known as facial detection, is a computer technology that uses artificial intelligence (AI) to find and recognize human faces in digital photographs. Face detection technology can be used to enable real-time surveillance and tracking of people in a variety of industries, such as security, biometrics, law enforcement, entertainment, and personal safety.

Face identification has advanced from simple computer vision approaches to increasingly complex artificial neural networks (ANN) and associated technologies, with the end result being constant performance gains. Face tracking, face analysis, and facial recognition are just a few of the significant applications it now serves as the starting point for. Sequential operations in the application will function significantly differently depending on face detection.


## Steps
Extraction of image frame
```bash
   # Capture the video
    video = cv2.VideoCapture(frame_list[idx])

    while(True):
        _, frame = video.read()
        
        # Handel the exception error
        try:
            train_image = cv2.resize(frame, (256,256), interpolation=cv2.INTER_AREA)
        except:
            break

        cv2.imshow("Train", train_image)
        
        # Saving the image to its corresponding dataset folders
        cv2.imwrite(directory+rf'{name_list[idx]}/'+str(current_frame)+'.jpg', train_image)
        length.append(current_frame)
        current_frame += 1

        interrupt = cv2.waitKey(10)
        if interrupt & 0xFF == 27: 
            break
    
    # Printing to see if the frame is successfully extracted
    print("Extraction for " + rf'{name_list[idx]}' + " completed!")
```
1. Creating a video frame
   Collect a video of the person you want to add into face detection system of atleast - 20 secs

2. Extracting image frame 
   Using open-cv extract the image frame from the videos
   
## How to use the code?
To get started with the project.
```bash
  git clone https://github.com/kinley2-glitch/face-detection-using-deep-learning
```

## Authors
- [kinley2-glitch](https://github.com/kinley2-glitch)

