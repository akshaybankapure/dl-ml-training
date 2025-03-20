### **Mini Project: Floorplan Room Segmentation using Open Source Dataset**

---

## **Objective**
Create a simple yet effective floorplan segmentation model that identifies rooms such as kitchens, bathrooms, and bedrooms using an open-source annotated floorplan dataset. The goal is to:

✅ Train a segmentation model.  
✅ Implement a prediction pipeline.  
✅ Visualize the model's output on new floorplans.  

---

## **Step 1: Dataset Selection and Preparation**
### Tasks
- Download an open-source annotated floorplan dataset. Recommended datasets:
  - [CubiCasa5K](https://github.com/CubiCasa/CubiCasa5k)
  - [R-FP Dataset](https://github.com/art-programmer/FloorplanTransformation)
- Extract image data and corresponding masks.
- Ensure images and masks are resized to a consistent resolution (e.g., `256x256` or `512x512`).
- Split the dataset into:
  - **Training Set** (70%)
  - **Validation Set** (15%)
  - **Test Set** (15%)

### Deliverable
✅ Dataset folder structure ready for model training.

---

## **Step 2: Data Augmentation and Preprocessing**
### Tasks
- Implement data augmentation using libraries like `Albumentations` or `imgaug` to improve model robustness.  
- Suggested augmentations:
  - Rotation
  - Flipping
  - Brightness and Contrast adjustments
  - Elastic transformation
- Normalize images and masks for consistent input range (e.g., 0-1 scaling).

### Deliverable
✅ Python script for data augmentation and preprocessing.

---

## **Step 3: Model Architecture**
### Tasks
- Use `nnUNet` or implement a lightweight U-Net from scratch for simplicity.
- Recommended architecture:
  - U-Net with batch normalization and `ReLU` activation.
  - Dice Loss for better segmentation performance on small room boundaries.
- Ensure the model outputs multi-class predictions for different room types.

### Deliverable
✅ Python file for model creation (`model.py`).

---

## **Step 4: Training Pipeline**
### Tasks
- Create a training pipeline using `PyTorch Lightning` or standard PyTorch training loop.
- Include:
  - Learning rate scheduler
  - Early stopping
  - Model checkpointing for best validation performance
- Visualize training loss and Dice score.

### Deliverable
✅ Python script for model training (`train.py`).  
✅ Graphs visualizing training/validation loss and metrics.

---

## **Step 5: Prediction Pipeline**
### Tasks
- Implement a simple inference pipeline that:
  - Loads a floorplan image.
  - Predicts the room types and visualizes the result.
- Overlay predicted masks on the original image.

### Deliverable
✅ Python script for prediction (`predict.py`).  
✅ Sample visualized results showcasing predicted rooms.

---

## **Step 6: Evaluation and Testing**
### Tasks
- Evaluate the model's performance on unseen test data.
- Use metrics such as:
  - Dice Coefficient
  - Intersection-over-Union (IoU)
- Compare performance between augmented and non-augmented data.

### Deliverable
✅ Python script for evaluation (`evaluate.py`).  
✅ Report summarizing model performance.

---

## **Step 7: Final Improvements**
### Tasks
- Add better visualization with matplotlib or OpenCV to overlay room types directly on the floorplan.
- Tune hyperparameters (learning rate, batch size) to improve performance.
- Test robustness by rotating, flipping, or resizing new floorplans.

### Deliverable
✅ Improved prediction pipeline with enhanced visualization.

---

## **Step 8: Deployment (Optional)**
### Tasks
- Wrap the prediction pipeline into a simple Flask API or FastAPI endpoint.
- Create a web UI where users can upload floorplan images and see predictions.

### Deliverable
✅ Web UI for easy floorplan room segmentation.

---

## **Project Folder Structure**
```
/floorplan_segmentation
    ├── data
    │   ├── train
    │   ├── val
    │   └── test
    ├── model.py
    ├── train.py
    ├── predict.py
    ├── evaluate.py
    ├── data_preprocessing.py
    ├── requirements.txt
    └── README.md
```

---

## **Timeline (By End of Week)**
| **Day** | **Task** |
|----------|------------|
| **Day 1** | Dataset download, preparation, and augmentation |
| **Day 2** | Implement U-Net model and start training |
| **Day 3** | Complete model training and visualize sample results |
| **Day 4** | Develop the prediction pipeline and test on new floorplans |
| **Day 5** | Evaluate model performance, improve visualizations, and summarize results |

---

## **End Result**
By the end of the week, the FSD will have:
✅ Successfully trained a floorplan segmentation model.  
✅ Developed a clean and structured codebase.  
✅ Created meaningful visualizations for model results.  
✅ Improved their understanding of nnUNet, data augmentation, and prediction pipelines.

---

Would you like a detailed code template for each file to help streamline the project further? 🚀
