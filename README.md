📰 Newspaper Blog Detection Using CNN and YOLO

This project focuses on automatically segmenting newspaper/blog page images into meaningful content regions such as Image areas, Title areas, Subtitle areas, and Text areas using a combination of Convolutional Neural Networks (CNN) and YOLO (You Only Look Once) object detection algorithm.

🔍 Objective

To develop a robust system that can detect and classify different content blocks in a newspaper layout image, enabling structured extraction and analysis of visual information from printed media.

🧠 Key Components
📦 Dataset

Custom-annotated dataset of newspaper/blog page images.

Each image is labeled with regions:

Image

Title

Subtitle

Text

🧮 CNN (Convolutional Neural Network)

Used in the early stages for feature extraction and region proposal.

Helps identify high-level semantic information like edges, contours, and shapes in content blocks.

⚡ YOLO (YOLOv8 Segmentation)

Used for real-time object detection and segmentation.

Detects and classifies each region in the newspaper image into its respective category (title, text, image, etc.).

YOLO’s segmentation variant (yolov8n-seg.pt or similar) is used to produce pixel-level masks, allowing precise boundary detection.

🧪 Training Configuration

Custom YOLO model trained on a small, manually labeled dataset.

Image augmentations applied to improve model generalization (e.g., flipping, scaling, HSV adjustments).

Evaluated on validation data using metrics like mAP (mean Average Precision).

✅ Output

Input: A scanned image or photo of a newspaper/blog page.

Output: The same image with detected blocks overlaid, each labeled as:

Title

Subtitle

Image

Text

📌 Applications

Automated content extraction for archiving and digital libraries.

Assisting OCR systems by feeding structured regions.

Enhancing news summarization and content indexing.

Useful in building AI-powered reading tools or mobile scanning apps.

🛠️ Tools & Technologies

YOLOv8 (Ultralytics) for segmentation

Python for scripting and preprocessing

OpenCV for image manipulation

Google Colab for model training and experimentation
