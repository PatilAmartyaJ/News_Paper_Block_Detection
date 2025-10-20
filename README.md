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
For eg:

### 1. Example: A news in Jammu

This image has one **Image Area** and one **Text Area**.  
The output image shows bounding boxes around each detected area.

#### 🔹 Input Image:
![Jammu](https://github.com/user-attachments/assets/c456f72f-fb25-407b-8d05-8d7c3142345a)


#### 🔹 Output with Bounding Boxes:
![result_Jammu](https://github.com/user-attachments/assets/e4b8fe62-fce2-4217-8fde-09c996ef7020)

### 2. Example: A news in Kolhapur

This image has one **Image Area** and 3 **Text Areas**.  
The output image shows bounding boxes around each detected area.

#### 🔹 Input Image:
![68952bcb44f97](https://github.com/user-attachments/assets/af732eef-6b28-4489-a6be-bcd8d5153c0b)


#### 🔹 Output with Bounding Boxes:
![result_68952bcb44f97](https://github.com/user-attachments/assets/8addde6b-d947-43cd-89fd-1a801a3f7ba5)

### 3. Example: A news in Amababai Temple in Kolhapur

This image has 2 **Image Area** and 3 **Text Areas**.  
The output image shows bounding boxes around each detected area.

#### 🔹 Input Image:
![Ambabai_original](https://github.com/user-attachments/assets/8b305071-f96e-4f63-bcdf-aad452a82bfe)



#### 🔹 Output with Bounding Boxes:
![annotated_Ambabai_original](https://github.com/user-attachments/assets/d10aef0f-b6e5-4003-8032-a666bc81fa08)





