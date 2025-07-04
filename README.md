POST = V3 (CURRENT VERSION)
V1 and V2 are solely there to show the evolution process

Hello, welcome to my nvidia project
This project uses the classification network system in order to monitor your posture and determine whether or not its correct or what needs to change
there are 3 classes: Good, Bad - Arched back (ARCH), and too close to the screen (CLOSE). This helps the user maintain good posture and understand how they can improve their posture in the future. As the human back and spinal cord is a very important part of the body, I believe this program is rather crucial in allowing people to maintain good health and posture whilst using electronic devices for long periods of time.


As VSCODE is currently bugged, the output will be class 0,1 or 2. (Training has been performed multiple times with no avail to insert correct classes)
All data has been collected by me using my own postures (1200 images per class)
The code runs on Resnet18, a classification artificial intellegence program which I have trained using my custom dataset that I have created myself.
There are 1200 images for each class with 3600 image inputs in total. This provides the AI with sufficient data to train and understand the differences between each posture, providing accurate results. The model then went through an 1000 epoch training session which lasted for approximately 10 hours, helping the AI to reach a high accuracy of approx 97%. 

A full demonstration of this model will be performed in the viideo linked below.

Beforehand, the following commands should be used in order to make the detection command usable:
NET=models/POSTURE32
DATASET=data/POSTURE32
(This defines terms in the script below)
This is the command that runs the program (Image jpg needs to be added to the end)
imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt 

steps:
A. download the model (POSTURE32 restnet18.onnx)
B. Insert the definition script (As seen above)

provide your own jpg file of your current posture (Drag and drop process shown in video)


https://drive.google.com/file/d/1p3TfcHyn_gmov_2kZkkgAaCfrEQr-Vgk/view?usp=sharing 
Demo Video link
