# Satellite Image Detection Using YOLOv8

![Satellite Detection](https://github.com/Nishant2018/YOLO-v8---Satellite-Image---Detection/blob/main/1_OGJeILFz3XjgiYP-7-IG-w.png)

This project demonstrates the detection of objects in satellite images using the YOLOv8 (You Only Look Once) model. The goal of the project is to identify objects like buildings, vehicles, and other significant features in satellite imagery.    
      
## Model Performance           
   
The YOLOv8 model has been trained on satellite images and achieved the following performance metrics:           
           
- **mAP (Mean Average Precision):** 59.3%           
- **Precision:** 60.0%     
- **Recall:** 59.6%  
      
## Dataset
    
The dataset used for training and evaluation consists of satellite images annotated with objects of interest. You can access the code from [Kaggle](https://www.kaggle.com/endofnight17j03).


## Getting Started

### Prerequisites

- Python 3.7+
- PyTorch
- YOLOv8 library

### Installation

1. Clone the repository:
   ```bash   
   git clone https://github.com/Nishant2018/YOLO-v8---Satellite-Image---Detection.git
   cd YOLO-v8---Satellite-Image---Detection
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

### Training the Model

To train the YOLOv8 model on satellite images, run the following command:
```bash
python train.py --data data/satellite.yaml --cfg yolov8.yaml --epochs 100
```

### Inference

To perform inference on new satellite images, run:
```bash
python detect.py --weights yolov8_best.pt --source data/test_images/
```

### Results

Once the model is trained, you can visualize the results using:
```bash
python visualize.py --results results/
```

## Project Structure

```bash
├── data/
│   ├── train/         # Training images
│   ├── test/          # Testing images
├── models/
│   ├── yolov8.yaml    # YOLOv8 model configuration
├── results/
│   └── images/        # Inference results
├── train.py           # Training script
├── detect.py          # Inference script
└── visualize.py       # Visualization script
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.


```
