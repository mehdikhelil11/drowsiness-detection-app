# Real-Time Drowsiness Detection System

[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)](https://tensorflow.org)
[![Keras](https://img.shields.io/badge/Keras-D00000?style=for-the-badge&logo=keras&logoColor=white)](https://keras.io)
[![OpenCV](https://img.shields.io/badge/OpenCV-27338e?style=for-the-badge&logo=OpenCV&logoColor=white)](https://opencv.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

Real-time driver drowsiness detection using deep learning - detects closed eyes and triggers an audio alert to prevent accidents.

---

## How It Works

```
Webcam Feed -> Face Detection -> Eye Region Crop -> CNN Classification -> Alert System
```

## Features

- Real-time detection via webcam using OpenCV
- - Ensemble model combining MobileNetV2 + ResNet for higher accuracy
  - - Audio alert triggered when eyes are detected as closed
    - - TFLite export for edge devices (Raspberry Pi, mobile)
      - - Two trained model formats: .keras (training) and .tflite (deployment)
        - - Trained on the CEW (Closed Eyes in the Wild) dataset
         
          - ---

          ## Model Architecture

          Input (Eye Region Image) -> MobileNetV2 Branch + ResNet Branch -> Ensemble Fusion -> Output: Open/Closed

          Training Dataset: CEW Dataset with closed/ and open/ eye image folders

          ---

          ## Tech Stack

          | Component | Technology |
          |---|---|
          | Deep Learning | TensorFlow / Keras |
          | Transfer Learning | MobileNetV2 + ResNet50 |
          | Computer Vision | OpenCV |
          | Edge Deployment | TensorFlow Lite (.tflite) |
          | Language | Python 3.9+ |

          ---

          ## Project Structure

          ```
          drowsiness-detection/
          |-- models/
          |   |-- AlertForClosedEyesModel.keras
          |   |-- mobilenet_resnet_ensemble.keras
          |   `-- EyesDetect_CEW_Final.tflite
          |-- data/
          |   `-- CEW/
          |       |-- closed/
          |       `-- open/
          |-- EyesDetectionNotebook.ipynb
          |-- EyesAppDL.py
          |-- app.py
          |-- SoundAlert.wav
          `-- README.md
          ```

          ---

          ## Installation

          ```bash
          git clone https://github.com/mehdikhelil11/drowsiness-detection-app.git
          cd drowsiness-detection-app
          pip install tensorflow opencv-python keras numpy pygame
          python EyesAppDL.py
          ```

          ---

          ## Use Cases

          - Driver safety systems
          - - Student attention monitoring in remote learning
            - - Workplace safety alerts
              - - Edge deployment with Raspberry Pi via TFLite
               
                - ---

                ## Author

                Mehdi Khelil - AI Engineer
                LinkedIn: https://www.linkedin.com/in/mehdi-khelil-a004a1225/
                GitHub: https://github.com/mehdikhelil11
                Email: mehdikhelil2204@gmail.com

                ---

                ## License

                MIT License - feel free to use and modify with attribution.
                
