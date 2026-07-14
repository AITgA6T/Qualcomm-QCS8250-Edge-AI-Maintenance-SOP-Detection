# Qualcomm QCS8250 Edge AI Maintenance SOP Detection

## Advantages of QCS8250

1.  RB3 Gen2 can provide up to 10 TOPS of AI computing power and supports GPU and DSP accelerated computing

2.  The Qualcomm Neural Processing (SNPE) SDK and the Qualcomm AI Engine Direct (QNN) can optimize the performance of trained neural networks

3.  It supports Android for AI development

## Performance Metrics

- **AI Model**:
- AI Model: YOLO-NAS、Mediapipe、HRNet

## Hardware

- **Platform**: Qualcomm QCS8250
- **Cameras**:  USB Camera × 1

## Software & Toolkit

- **AI SDK (SNPE) SDK**： v2.16.0.231029

## Background & Solution

### Motivation:
- Traditional equipment maintenance often relies on manual inspection and centralized processing which would be resulted in delayed responses and difficulty detecting incorrect maintenance procedures in real time. Edge AI enables on-device SOP detection, improving maintenance efficiency, reducing human errors, and ensuring reliable equipment operation

### Solution:
- Using the QCS8250 as the core platform, integrating Edge AI and real-time control to deploy lightweight AI models for on-device maintenance SOP feature extraction and procedure detection, and enabling real-time monitoring, anomaly alerts, and automated maintenance management.

## Architecture Diagram:

The camera captures real-time video streams, and all image processing is performed directly on the QCS8250.  
YOLO-NAS is used to detect operators, tools, and equipment, while MediaPipe extracts human body keypoints. HRNet then performs pose analysis and maintenance SOP action recognition to verify whether each maintenance step follows the standard operating procedure.
All processing takes place on the edge device, ensuring better privacy and data protection



<img src="QCS8250 維修SOP.assets/media/2.PNG"/>

### Demo:

<img src="QCS8250 維修SOP.assets/media/demo.gif" width="720" />

