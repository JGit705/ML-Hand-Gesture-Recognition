# ML-Hand-Gesture-Recognition

This project implements a static hand gesture classification system using convolutional neural networks (CNNs), trained via transfer learning on pre-trained **ResNet-18** and **AlexNet** models in MATLAB. The system recognizes five distinct gestures: ✌️ Peace, 👍 Thumbs Up, 👌 Okay, ❤️ Heart, ✊ Fist.

## Project Structure

```
Hand-Recognition-Project/
│
├── AlexNet 2024-5.mlx            # AlexNet training & evaluation script
├── ResNet18 2024-5.mlx           # ResNet-18 training & evaluation script
├── Image Prediction 2024-5.mlx   # Real-time image prediction tool
├── Hand Gesture Recognition Report.pdf  # Full project report
├── models/                       # Trained .mat models (ignored in Git)
├── dataset/                      # Image dataset (not pushed to GitHub)
└── README.md
```

## Features

- MATLAB-based implementation using Deep Learning Toolbox
- CNN transfer learning using ResNet-18 and AlexNet
- Data augmentation (rotation, shear, flipping, scaling)
- Real-time image classification with confidence scoring
- Evaluation via accuracy, precision, recall, F1-score, confusion matrix, and ROC curves

## How to Run

1. Clone the repository:

   ```bash
   git clone git@github.com:JGit705/ML-Hand-Gesture-Recognition.git
   ```

2. Open MATLAB and navigate to the project directory.

3. Run the training script:

   - For ResNet-18:
     ```matlab
     open('ResNet18 2024-5.mlx')
     ```
   - For AlexNet:
     ```matlab
     open('AlexNet 2024-5.mlx')
     ```

4. Use the prediction tool:

   ```matlab
   open('Image Prediction 2024-5.mlx')
   ```

5. Load test images and run prediction to get gesture classification with confidence levels.

> ⚠️ `.mat` model files are excluded from GitHub due to file size limits. You must train or request models separately.

## Performance

| Model     | Accuracy | F1-Score (avg) | Best Class | Weakest Class |
| --------- | -------- | -------------- | ---------- | ------------- |
| ResNet-18 | 91.6%    | ~0.92          | ❤️ Heart   | 👌 Okay       |
| AlexNet   | 80.5%    | ~0.81          | ❤️ Heart   | 👌 Okay       |

- ROC AUC > 0.9 for all classes (ResNet outperformed across metrics)
- Real-time prediction tool supports image uploads with visual scoring

## Dataset

- 5,000 RGB gesture images from [HAGRiD](https://github.com/hukenovs/hagrid)
- 5 gesture classes, 1,000 images each
- Preprocessed to 224×224 or 227×227 input sizes
- Augmented using `imageDataAugmenter` in MATLAB

## Evaluation Tools

- `confusionchart`, `plotroc`, `classify`, `precision`, `recall`, `f1-score`
- Visual model comparison via confusion matrices and ROC curves

## Limitations

- Static image input only (no video or dynamic gestures yet)
- Limited gesture set (5 gestures)
- No user diversity testing

## Future Work

- Add dynamic gesture recognition (e.g., RNN/LSTM)
- Expand gesture vocabulary (fingerspelling, sign language)
- Integrate live webcam input
- Improve model robustness under real-world conditions
- Deploy to edge devices or embedded systems

## Contributors

- Jamal Lharri
- Karim Poonawala
- Aidan Pereira
- Jay Revagar
- Sharaf Ahamed Shareef
- Joji Kondo

_Supervised by Dr QingPing Yang_ Brunel University London
