NOTE:- The   IoU  Confidence  Precision    Recall  F1-Score and map50 is not showing good score just because YOLO cant predict on .TIF extension image since all the images in the dataset was not jpg format so i converted only 30 images from tif to jpg as i cant find any software that convert 3000 image at once so the score is on 30 images . i can improve the score as i will get the images in the jpg format 
Data Exploration & Understanding
✅ Load Dataset
Images are provided in 416x416 resolution.
Labels are in MS-COCO format with Horizontal Bounding Boxes (HBB).
✅ Compute Dataset Statistics
Count the total instances of solar panels in the dataset.
Compute label frequency:
Calculate the area of solar panels (in meters):
Compute mean area and standard deviation.
Plot a histogram of the areas to observe distribution.

2️⃣ Implementing Key Functions

✅ Compute IoU (Intersection over Union)
IoU measures overlap between ground truth and predicted bounding boxes.

✅ Compute Average Precision (AP)
Pascal VOC 11-point interpolation
COCO 101-point interpolation
Area under Precision-Recall Curve (AP)
Test AP calculations by:
Comparing AP50 (IoU 0.5) scores for the three methods.

3️⃣ Model Building & Evaluation
✅ Train an Object Detection Model
Split Data:
80% Train, 10% Test, and 10% for Validation.
Use YOLO (Ultralytics) for Training:
Train the model on the dataset.
Show that validation loss converges 
The trained model is validated on test images to compute various performance metrics.
4️⃣ Model Predictions & Visualization
Now you need to test and visualize how well the model performs.
✅ Predict and Visualize Results
5️⃣ Compute Evaluation Metrics
Now, compare your own implementation with standard libraries.
✅ Compute mAP50
✅ Precision, Recall, and F1-score Table
