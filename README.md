# Odometer Detection
This project aimed to extract the odometer part from the car's dashboard images.

The task contained two parts. First of all, we should detect the odometer part from the car's dashboard images and after that, use this part to extract the odometer number.

## DATASET
The dataset contained 118 images of the car's dashboard.


## Odometer Detection Using YOLOv8
For this part, I used [YOLOv8](https://docs.ultralytics.com/). But at first, I needed to prepare the dataset for this part. So, I utilized the [Labellmg](https://github.com/HumanSignal/labelImg/releases) tool for labeling the images. I have 118 images and among these images, 1 image was ignored because of low quality and weak information. I separate 17 images for validation.

### Result Of the Model


### Extract Text from Images
Now, we can detect odometers from images. So, I used the best model to detect the odometer part from images and cropped that part for the rest of the operations. After cropping the odometer part, I feed this part to easyOCR for text extractions. In this link, you can see these processes. Before feeding images to easyOCR, I applied some preprocessing to images.

### Conclusion of easyOCR


### Utilize PaddleOCR


## Trained My OCR Model



