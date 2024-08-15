# dog-emotion-recognition-AI
This model classifies dogs with emotions of anger, sadness, relaxation, and happiness.This model is likely to be of great help to dog lovers who need to identify dog's emotions.
 


![image](https://github.com/user-attachments/assets/d9561753-9366-41e1-8700-698378958e54)

## The Algorithm
It is a re-trained ResNet-18 model which was trained on a dataset of 4000 images of dogs with different emotions. This project works by classifying images with ImageNet. 

## Running this project

1. Make sure that both the Jetson Inference library and Python3 are installed on your Jetson Nano.
2. You can download jetson inference on https://github.com/imnotleo666/jetson-inference.
3. Open the terminal and navigate to the classification directory:

   $ cd jetson-inference/python/training/classification

4. Set the net and data variables as shown below:

   $ NET=models/snake

   $ DATASET=data/snake3
   
5. Use this command to process an image:

   $ imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt $DATASET/test/angry/0rAH60FVXqnFBJPzGVSxzEe22APpFS734.jpg dog1.jpg
   
6. additionnally, if you would like to use your own images of dogs, add them to one of the directories under the test directory and use the above command and edit "angry/0rAH60FVXqnFBJPzGVSxzEe22APpFS734.jpg" accordingly to the folder and name of your image.

6.Lastly, check the ouput see the classification.

[View a video explanation here](video link)
