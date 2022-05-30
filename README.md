# MILITARY AIRCRAFT DETECTION WITH YOLOV5
Problem: In this project, the aim was detecting 36 different military aircraft model and classifying them accordingly.


The dataset used for training and test can be found in Kaggle: [https://www.kaggle.com/tawsifurrahman/covid19-radiography-database](https://www.kaggle.com/datasets/a2015003713/militaryaircraftdetectiondataset)

Solution: We derived a solution from the current YOLOv5 implementations out there in github from [Ultralytics](https://github.com/ultralytics/yolov5). It was useful for us to learn parameters and also comment on the test metrics.

You can see the demonstration with data in the result files we placed in the repository.

# Training Result
![results](https://user-images.githubusercontent.com/59517900/171016253-4c40b6ca-956c-4914-b55c-e050ef496e3b.png)


# Labels and Predictions
  It's obvious that our model lacks some ability in detecting small objects. So we need to work more on that to figure that out.  
Labels:  
![val_batch1_labels](https://user-images.githubusercontent.com/59517900/171016428-81cf46b3-a8f6-4b67-b2d4-20eea586fc7d.jpg)
Predictions:  
![val_batch1_pred](https://user-images.githubusercontent.com/59517900/171016437-1bbf733a-0f9b-436d-831d-72e82e89db79.jpg)

# Confusion Matrix
Confusion matrix shows us that we were most of the time good at classifying aircrafts and since there were 36 classes overall we were on a good place.  
![confusion_matrix](https://user-images.githubusercontent.com/59517900/171016759-c7cfac60-4da6-44f3-ba86-fc5889097c02.png)

# Final Results [100th Epoch]
Precision: 0.73879  
Recall   : 0.81919  
```
               epoch	      train/box_loss	      train/obj_loss	      train/cls_loss	   metrics/precision	      metrics/recall	     metrics/mAP_0.5	metrics/mAP_0.5:0.95	        val/box_loss	        val/obj_loss	        val/cls_loss	               x/lr0	               x/lr1	               x/lr2
												
99	       0.012802	    0.0079659	       0.0049855	      0.82872	           0.73879	            0.81919	          0.73181	           0.015661	              0.0065615	         0.030865	         0.000298	             0.000298	              0.000298

```

# Comments

This project still needs to be improved for small objects and higher precision & recall.

-Avion AI
