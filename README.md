- Processed Outputs: https://drive.google.com/drive/folders/1fKk-T4FfbX3paHAIsPTZayt3c5E50vXm?usp=sharing
- Final Report: https://drive.google.com/drive/folders/1mPVWEv5yONlYTaBCOUJT1juWLYLYoC2A?usp=sharing
- Screen Recording: https://drive.google.com/file/d/1SbMmdIYYtfWn6QC5I36gyLj6d410ZY8a/view?usp=sharing

Train Video Processing – Automated Wagon Segmentation & Coverage Report
Overview

This project implements a computer vision pipeline to analyze train side-view CCTV footage.
The system automatically:

Segments the input video into engines, wagons, and brakevan

Counts all train units accurately

Extracts a minimal set of coverage frames per segment

Performs door detection on engines only (wagons are transfer blocks without doors)

Generates a structured PDF report with a train summary and annotated images

This work was developed as part of an assignment on train video analysis.

Features

Video Segmentation – Split continuous train footage into smaller clips (per engine/wagon/brakevan)

Train Counting – Count and label all units with unique IDs (e.g., 12309_engine_1, 12309_coach_1, …)

Frame Extraction – Save 3 representative images per unit to ensure full visual coverage

Door Detection (Engines) – Detect open/closed doors on locomotives only

Final Report Generation – Structured PDF with train summary and annotated images

Project Structure
train-video-processing/
│
├── train_processing.ipynb     # Colab notebook (main pipeline)
├── requirements.txt            # dependencies
├── README.md                   # project overview & setup
└── .gitignore                  # exclude large files (videos, processed data)


When executed, outputs are stored in:

train_project/
│
├── raw_videos/                # input videos
├── processed/                 # outputs
│   ├── 12309_engine_1/        # frames + annotated images
│   ├── 12309_coach_1/
│   ├── ...
│   ├── 12309_brakevan_1/
│   └── 12309_final_report.pdf # submission-ready report

Setup & Usage
Run on Google Colab (recommended)

Open train_processing.ipynb in Google Colab

Mount Google Drive

Upload raw train video(s) to /train_project/raw_videos/

Run all cells sequentially

Processed outputs and final PDF report will be saved in /train_project/processed/

Run Locally
# clone repo
git clone https://github.com/<your-username>/train-video-processing.git
cd train-video-processing

# install dependencies
pip install -r requirements.txt

# run notebook
jupyter notebook train_processing.ipynb

Outputs

Segmented videos – per engine/wagon/brakevan

Coverage frames – 3 images per segment

Annotated images – doors on engines (open/closed)

Final PDF report – summary and per-segment details

Notes & Assumptions

This dataset represents a transfer train – wagons do not have passenger doors.

Door detection is only applied to engines.

All coaches/wagons and the brakevan are reported with zero doors.

Submission Requirements

Code → GitHub repo (this project)

Processed outputs → Google Drive (Processed_Video/)

Final report → Google Drive (Final_Report/)

Screen recording → Short video walkthrough of pipeline and outputs

Author: Isha Chaturvedi

