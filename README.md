

# YOLO demo


##  See following website for the explanation of this demo

--> [medium.com](https://dipankarmedh1.medium.com/real-time-object-detection-with-yolo-and-webcam-enhancing-your-computer-vision-skills-861b97c78993)

## Install the requirements:

```commandline
    pip install -r requirements.txt
```

## Select model:

To select the model you need to change the uncommented line on lines 16 tot 20.

## Select camera input:

To change the camera from the default (id = 0) webcam, you need to change the id on line 5 untill you find the correct id.
This can take a bit.
(These seem to be relatively low values, I once had 2 and another time 3 for my external camera.)

## Change resolution:

This is possible, although my webcam was not capable of more than 640 by 480 at 60FPS, 
and my USB webcam does go to 1080p, but only at about 5 FPS.
You can uncomment lines 11 and 12 to manually experiment with higher resolutions.
Be aware that my bottleneck seems to be the USB camera and the bitrate available over USB, your millage will vary.

## About the refreshrate:

The refreshrate is selected by the opencv-python library, and if you get stuck on a low refreshrate,
just make sure you have enough light available.
If that's not the case it is possible that the camera can't deliver a higher framerate or
that the connection is limited by USB speeds.



## Troubleshooting: checking camera compatibility

To check if the camera is working, you can run CameraTest.py,
this should just show the camera feed of the webcam on a laptop.