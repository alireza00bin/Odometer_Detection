# Odometer Detection
This project aimed to extract the odometer part from the car's dashboard images.

The task contained two parts. First of all, we should detect the odometer part from the car's dashboard images and after that, use this part to extract the odometer number.

## DATASET
The dataset contained 118 images of the car's dashboard.
![](https://github.com/alireza00bin/Odometer_Detection/blob/main/photos/Car_Dashborad_Image.jpeg)

## Odometer Detection Using YOLOv8
For this part, I used [YOLOv8](https://docs.ultralytics.com/). But at first, I needed to prepare the dataset for this part. So, I utilized the [Labellmg](https://github.com/HumanSignal/labelImg/releases) tool for labeling the images. I have 118 images and among these images, 1 image was ignored because of low quality and weak information. I separate 17 images for validation.


### Result Of the Model
![](https://github.com/alireza00bin/Odometer_Detection/blob/main/photos/download.jpeg)


### Extract Text from Images
Now, we can detect odometers from images. So, I used the best model to detect the odometer part from images and cropped that part for the rest of the operations. After cropping the odometer part, I feed this part to easyOCR for text extractions. In this link, you can see these processes. Before feeding images to easyOCR, I applied some preprocessing to images.


### Conclusion of easyOCR
#### True Detection
![](https://github.com/alireza00bin/Odometer_Detection/blob/main/photos/OCR_True_Detection.png)

#### False Detection
![](https://github.com/alireza00bin/Odometer_Detection/blob/main/photos/OCR_False_Detection.png)


### Utilize PaddleOCR


### Trained My OCR Model
I tried to build a CRNN and trained the model on the custom dataset. Because of the lack of data, I could not train further.


