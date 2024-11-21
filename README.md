# Cell-segmentation-with-YOLO-algorithm-and-semisupervised-learning

In the field of medical image analysis, it is common to encounter a large amount of unlabeled data, while labeled data is scarce. Additionally, the labeling process must be carried out by specialists with several years of experience, which increases both complexity and associated costs. For this reason, semi-supervised learning emerges as a promising solution, as it enables medical image segmentation algorithms to leverage both labeled and unlabeled data.  

This project implements **AutoTraining** in a YOLO model from Ultralytics, using and referencing the implementation presented in [1] for the NulnsSeg Kaggle dataset [2]. The algorithm's training was conducted in four main stages:

* Supervised training of the algorithm using 80% of the data as the training set and 20% as the test set.  
* Supervised training of the algorithm with only 10% of the data as the training set and 20% as the test set, leaving the remaining 70% unlabeled.  
* Automatic labeling of the unlabeled data using the supervised model trained with 10% of the data.  
* Supervised training of the algorithm combining the original 10% labeled data with the data automatically labeled in the previous stage.

This is an educational project, so the method was not evaluated using different folds, and the data was only split into training and test sets. The code was executed in the Google Colab environment with an A100 GPU.

  [1] LearnOpenCV. (2024). YOLOv9 instance segmentation on medical dataset. LearnOpenCV. https://learnopencv.com/yolov9-instance-segmentation-on-medical-dataset/
  
  [2] IPATeam. (2023). NUINSSeg dataset [Archivo de datos]. Kaggle. https://www.kaggle.com/datasets/ipateam/nuinsseg
