# Object-Detection-
Object detection using the custom dataset using the YOLOv4 in the Google Colab
You could download the dataset from kaggle used in this repo using the link : https://www.kaggle.com/sakshamjn/vehicle-detection-8-classes-object-detection 
### Code :
follow the youtube video by The AI Guy for step by step guide : https://www.youtube.com/watch?v=mmj3nxGT2YQ

### Data preprocessing
First put all images (.jpg) and labels (.txt) in one folder as shown below.
![image](https://user-images.githubusercontent.com/75324891/150961520-1af10363-b058-478b-ad5f-e75995924510.png)

Given train dataset first divided into the train and validation dataset in 80 % and 20 % respectively using the jupyter notebook on the local machine using the file named “YOLOv4_data_preprocessing.ipynb” in the following structure:

Images
➔	Train(.jpg)
➔	Val(.jpg)
Labels
➔	train(.txt)
➔	val(.txt)

 Then manually the data is made in the following format for the YOLOv4 algorithm required

Dataset
➔	obj(.jpg and .txt)
➔	test(.jpg and .txt)

![image](https://user-images.githubusercontent.com/75324891/150959933-e8b71edb-6f62-42b3-ad14-20921c4a3cca.png)


### Steps to do the the Objection using the google colab: Follow the Youtube video by The AI Guy
### Results from the Custom object detection by YOLOv4

### Accuracy of custom trained :
	


detections_count = 33774, unique_truth_count = 5313  


![image](https://user-images.githubusercontent.com/75324891/150963232-49cc52ae-5c3e-490f-9e31-6a5a3d25d9ad.png)


 for conf_thresh = 0.25, precision = 0.61, recall = 0.84, F1-score = 0.71 
 for conf_thresh = 0.25, TP = 4445, FP = 2839, FN = 868, average IoU = 45.73 %

IoU threshold = 50 %, used Area-Under-Curve for each unique Recall 
mean average precision (mAP@0.50) = 0.641146, or 64.11 % 
Total Detection Time: 30 Seconds

YOLOv4 algorithm performed quite well on the given dataset.


Testing the custom Algorithm on validation images:


![image](https://user-images.githubusercontent.com/75324891/150962260-b396cb29-9ac2-423b-89c8-37fbfbd25edd.png)


![image](https://user-images.githubusercontent.com/75324891/150962412-dae4b2cd-0aa5-4f6e-9413-86685c3e286b.png)


![image](https://user-images.githubusercontent.com/75324891/150962459-78052e51-975f-43d9-b8b3-ff5dc3841a72.png)


## Future Scope:

We can see YOLOv4 algorithm is a faster and more accurate object detection algorithm. But here we can improve the custom algorithm by:
1.	Run the Algorithm for more number of iteration and stop when the model starts to overfit.
2.	To avoid the Class imbalance present in our dataset we can adopt Data Augmentation techniques i.e. generate more images of the classes having fewer training samples by rotating, flipping, translating, etc.

