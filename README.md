# Novius_PROJECT_
Deep learning project
# Flask PPE Detection Project

This repository contains the Flask-based web application for detecting Personal Protective Equipment (PPE) using the YOLOv8 model. The application is designed to analyze video input and identify the presence of PPE, such as helmets, gloves, and other safety gear.

## Features

- **YOLOv8 Detection Model**: Efficient and accurate object detection.
- **10 PPE Classes**: Trained on a dataset with over 700 images.
- **Real-Time Detection**: Analyze video input for PPE compliance.
- **Data Storage**: Detection results are stored in a MySQL database.
- **Flask Web Application**: Simple web interface for uploading and analyzing video files.

## System Workflow

1. User uploads a video through the web interface  
2. The system processes the video frame by frame  
3. YOLOv8 model detects PPE items  
4. Detected objects are labeled with confidence scores  
5. Results are displayed with bounding boxes  
6. Detection data is stored in the MySQL database  

## Prerequisites

Make sure you have the following installed:

- Python 3.8+
- MySQL Server
- Required Python libraries (listed in `requirements.txt`)

## Dataset

The dataset used for training the YOLOv8 model is hosted on [Roboflow](https://roboflow.com/). You can download the dataset using the link below:
https://universe.roboflow.com/roboflow-universe-projects/construction-site-safety/dataset/28


## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/sakshi272004/TYPROJECT_PPE_DETECTION
   cd your-repo-name
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Configure MySQL:
   - Create a MySQL database.
   - Update the database credentials in `flaskapp.py`.

4. Run the Flask application:
   ```bash
   python flaskapp.py
   ```

5. Open the application in your browser:
   ```
   http://127.0.0.1:5000
   ```
## Creating an Executable File

To distribute your project as a standalone `.exe` file, follow these steps:

1. Install PyInstaller:
   ```bash
   pip install pyinstaller
   ```

2. Convert the Python script to an executable:
   ```bash
   pyinstaller --onefile --windowed app.py
   ```

3. The `.exe` file will be located in the `dist` folder. Share this file for easy execution without requiring Python installation.

## Usage

- Upload a video file via the web interface.
- The system will analyze the video and display detection results.
- Results, including detected PPE classes and confidence scores, will be stored in the MySQL database.

## Output

- Bounding boxes around detected PPE items  
- Labels such as Helmet, Gloves, Vest, etc.  
- Confidence score displayed for each detection  
- Detection results stored in MySQL database  

## Project Structure

```
.
├── flaskapp.py           # Flask application
├── YOLO_Video.py         # detection file
├── requirements.txt      # Required Python libraries
├── templates/            # HTML templates for the web interface
├── static/               # Static assets (CSS, JS, images)
├── YOLO_Weights/         # YOLOv8 model files              
└── README.md             # Project documentation
```

## Suggestions for Improvement

1. **Dataset Expansion**:
   - Include more diverse PPE images for improved detection.

2. **Model Optimization**:
   - Experiment with model compression techniques for faster inference.

3. **Real-Time Video Streaming**:
   - Add support for analyzing live video streams.

4. **Advanced Analytics**:
   - Integrate advanced analytics and visualizations for detection data.

5. **Deployment**:
   - Host the application on a docker for remote accessibility.
  
## Challenges & Solutions

- **Challenge:** Real-time video processing  
  **Solution:** Optimized frame handling using OpenCV  

- **Challenge:** Detection accuracy  
  **Solution:** Used a trained dataset with multiple PPE classes  

- **Challenge:** Data storage and management  
  **Solution:** Integrated MySQL database for structured logging  

## License

This project is licensed under the [MIT License](LICENSE).

---

For any questions or suggestions, please feel free to open an issue or contact me directly!
