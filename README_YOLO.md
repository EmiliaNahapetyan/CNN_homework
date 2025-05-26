# YOLOv8 Object Detection Demo (Pascal VOC Fine-Tuned)

This project demonstrates how to run object detection using a YOLOv8 model fine-tuned on the Pascal VOC dataset. 

## 🧰 Requirements

This script is intended to run in **Google Colab**.

Install the required libraries in Colab:

```bash
pip install ultralytics opencv-python
```

## 📁 Project Structure

```
├── detection_demo.py         # Main detection script
├── YOLOv8n_PascalVOC/        # Folder with fine-tuned YOLOv8 model
│   └── weights/
│       └── best.pt           # Fine-tuned model weights
├── output_video.mp4          # (Optional) Output video after detection
```

## ▶️ Usage Instructions

### Option 1: Detect from a local video path

Modify the script or run with the following arguments:

```python
!python detection_demo.py   --mode video   --source /path/to/your/video.mp4   --model /content/YOLOv8n_PascalVOC/weights/best.pt   --output_video output_video.mp4
```

### Option 2: Detect from a YouTube link

```python
!python detection_demo.py   --mode youtube   --source https://www.youtube.com/watch?v=YOUR_VIDEO_ID   --model /content/YOLOv8n_PascalVOC/weights/best.pt   --output_video output_video.mp4
```

> **Note:** You must add functionality to download the YouTube video in the script, e.g., with `pytube`.

### Option 3: Upload a video manually

```python
!python detection_demo.py   --mode upload   --model /content/YOLOv8n_PascalVOC/weights/best.pt   --output_video output_video.mp4
```

The script will prompt you to upload a video file using Colab's interface.

## 🧪 Model

The model used is a fine-tuned YOLOv8n trained on the Pascal VOC 2007 dataset. Make sure the `best.pt` weight file is located in:

```
/content/YOLOv8_VOC_FineTune/YOLOv8n_PascalVOC/weights/best.pt
```

You can adjust the `--model` argument if your model path is different.

## 📤 Output

The script will:
- Process frames one-by-one
- Annotate detections
- Automatically download the result to your local machine (if running in Colab)

## 📌 Notes

- This demo is built specifically for YOLOv8 models using the `ultralytics` library.

---

## 📷 Example Output

```bash
100 frames processed...
200 frames processed...
```

---
