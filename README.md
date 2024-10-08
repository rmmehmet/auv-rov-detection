## Unmanned Underwater Vehicle Detection with YOLOv5

### YOLO

YOLO (You Only Look Once) is a state-of-the-art, real-time object detection system. It frames object detection as a single regression problem, straight from image pixels to bounding box coordinates and class probabilities.

Key Features of YOLO:

* Speed: YOLO is incredibly fast because it only looks at the image once (hence the name) to predict what objects are present and where they are.
* Unified Architecture: It uses a single neural network to perform classification and localization tasks simultaneously.
* High Accuracy: Despite its speed, YOLO maintains high accuracy, making it suitable for real-time applications.
* Generalization: YOLO generalizes well to new domains, which makes it an effective solution for a variety of detection tasks.

YOLO divides the image into a grid and predicts bounding boxes and probabilities for each grid cell. This approach allows YOLO to understand the global context of the image, making it particularly effective for detecting large objects or groups of objects.

### Model
<br>
<div align="center">
<img src="yolov5_x\yolov5\yolov5-performance.png">
<br>
<i>Yolov5 Model Performance</i>
</div>
<br>
Yolov5 version x model was used in this project. The YOLOv5 x (extra large) model has certain advantages when compared to other YOLOv5 models (n, s, m, l). Here are some areas where the YOLOv5x model stands out compared to others:

* Higher Accuracy: YOLOv5x, being a larger model, can learn more complex and detailed features. This is particularly useful for recognizing small objects or achieving higher accuracy in complex scenes.

* Larger Model Capacity: YOLOv5x has more parameters and layers. This allows the model to generalize better when trained on a wider dataset.

* Detailed Feature Maps: The model’s width and depth enable it to generate more detailed and rich feature maps. This is especially beneficial for detecting very small objects.

* Superiority in Challenging Tasks: YOLOv5x performs better in more complex and challenging tasks (e.g., high-resolution images or scenes with a large number of objects).

However, YOLOv5x also has some disadvantages:

* Higher Computational Power Requirement: YOLOv5x, being larger than other models, requires more computational power and memory. This can be a disadvantage, especially for low-power devices or real-time applications.

* Longer Training Time: YOLOv5x has more parameters, so the training and inference process takes longer.

* Higher Hardware Requirements: YOLOv5x, especially in terms of GPU requirements, needs more powerful hardware.

* In conclusion, the YOLOv5x model is advantageous in tasks requiring high accuracy and more complexity. However, these advantages are balanced by increased computational requirements and longer processing times. If your goal is high accuracy, YOLOv5x might be an ideal choice, but if you need a faster and lighter model, it may be better to opt for one of the other models.

### Example Detection
<br>
<div align="center">
<img src= "yolov5_x\yolov5\auv_output-1.png">
<br>
<i>Auv - Rov Detection</i>
</div>
<br>
<div align="center">
<img src= "yolov5_x\yolov5\auv-test-image.jpg">
<br>
<i>Auv - Rov Detection</i>
</div>
<br>

### Graphic From the Training Process

<div align="center">

<img src= "yolov5_x\yolov5\results.png">
<i>Model Results</i>
</div>
<br>

1. train/box_loss 

* This graph shows the error the model experiences while learning bounding boxes for object detection. The graph indicates that the error decreases during the training process, meaning the model is detecting objects more accurately over time.

2. train/obj_loss 
* This graph represents the error the model makes when predicting the presence of an object. The decreasing trend of this loss over time suggests that the model is increasingly accurate in recognizing objects.

3. train/cls_loss 
* This graph shows the error the model makes when classifying objects (for example, identifying whether an object is a dog or a cat). The fact that this loss remains flat indicates that either the model is not performing classification or there is no error in the classification aspect of the dataset.

4. val/box_loss 
* This graph shows the model's bounding box error on the validation dataset. The decreasing trend of this loss during the training process indicates that the model is also performing well on validation data.

5. val/obj_loss 
* This graph shows the error in object detection on the validation data. The loss decreases and stabilizes over time, suggesting that the model is generally consistent.

6. val/cls_loss 
* Similar to the training classification loss, this graph remains flat, indicating that either classification is not part of the model or there is no error in this section on the validation data as well.

7. metrics/precision 
* This graph shows the model's precision. The graph indicates that precision increases over time and reaches a high level. This means that a large portion of the objects detected by the model are correctly classified.

8. metrics/recall
* This graph shows the model's recall. The graph indicates that recall increases and stabilizes over time. This implies that the model has a high ability to recognize true positives.

9. metrics/mAP_0.5 
*This graph shows the model's mean average precision (mAP) at an IoU threshold of 0.5. The graph indicates that the model's mAP is quite high and improves over time, suggesting good overall performance.

10. metrics/mAP_0.5:0.95 
* This graph shows the model's mean average precision (mAP) across different IoU thresholds. The graph indicates that the model has been tested at a variety of thresholds and performs well overall.

Model Evaluation

* Based on these graphs, the model shows progressively better performance during both the training and validation phases. The decrease in losses and the increase in metrics (precision, recall, mAP) indicate that the model successfully detects objects and has a strong generalization capability. The training process has progressed well, and the model has also demonstrated successful performance on the validation dataset.

<br>
<div align="center">
<img src= "yolov5_x\yolov5\labels_correlogram.jpg">
<i>Labels Correlogram Graph</i>
</div>
<br>
The graphs in this image are a type of graph known as a correlogram (pairplot) and are used to show the distance between distributions of different variables. It is used to visualize connections in the data set during exploratory data analysis.

### Model and Dataset

You can access the trained YOLOv5 model and the created AUV-ROV dataset through this link:

<div align="center">
<a href="https://drive.google.com/drive/folders/1KT9_yOA-bU6BIuaIy1PZyUFe0oRPRKjA?usp=drive_link" target="_blank">Trained YOLOv5x Model and Generated AUV-ROV dataset
</a>

</div>