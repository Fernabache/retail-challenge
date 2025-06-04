# Retail Challenge Submission (Final)

## Setup Instructions
1. **Open Google Colab**: Create a new notebook at [colab.research.google.com](https://colab.research.google.com) with GPU enabled (`Runtime` > `Change runtime type` > `T4 GPU`).
2. **Upload Files**:
   - Upload `annotations.json` to `/content/`.
   - Mount Google Drive: Run the notebook’s `drive.mount` cell and authenticate.
   - Ensure videos are in `/content/drive/MyDrive/retail_challenge/videos/`.
3. **Install Dependencies**: Run the first cell to install `tensorflow`, `opencv-python-headless`, `matplotlib`, `pandas`, and `seaborn`.
4. **Run Notebook**: Execute all cells (`Runtime` > `Run all`). The notebook fine-tunes MobileNetV2, processes a subset of videos (with frame sampling), calculates activity durations, and generates visualizations.
5. **Outputs**: Download `/content/mobilenetv2_finetuned.weights.h5`, `activity_durations.csv`, `stacked_bar.png`, and `gantt_timeline.png`.

## Requirements
- Google Colab with free GPU (T4).
- Google Drive with video files.
- Runtime: ~16-21 minutes .
- Outputs: Fine-tuned weights, activity durations CSV, stacked bar chart, Gantt timeline.

## Notes
- Adjust `video_dir` if the video folder path differs.
- Frame sampling (`max_frames=16`) ensures runtime <25 minutes.
- Fine-tuning uses 30 segments from 2 videos; inference on 5 videos.
- Adjust `max_segments` or video counts for runtime/accuracy trade-off.
