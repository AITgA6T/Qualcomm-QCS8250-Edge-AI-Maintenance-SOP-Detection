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

- 傳統設備維護主要依賴人工檢查與中央系統分析，容易產生延遲，且無法即時發現操作流程錯誤。透過 Edge AI 可在裝置端即時辨識維護 SOP 執行情況，提升維護效率、降低人為失誤，並確保設備運作可靠性。
- Traditional equipment maintenance often relies on manual inspection and centralized processing which would be resulted in delayed responses and difficulty detecting incorrect maintenance procedures in real time. Edge AI enables on-device SOP detection, improving maintenance efficiency, reducing human errors, and ensuring reliable equipment operation

### Solution:

- 以 QCS8250 為核心，整合 Edge AI 與即時控制技術，部署輕量化 AI 模型，在裝置端進行維護 SOP 特徵擷取與流程辨識，實現即時監測、異常警示及自動化作業管理。
- Using the QCS8250 as the core platform, integrating Edge AI and real-time control to deploy lightweight AI models for on-device maintenance SOP feature extraction and procedure detection, and enabling real-time monitoring, anomaly alerts, and automated maintenance management.

## Architecture Diagram:

The camera captures real-time video streams, and all image processing is performed directly on the QCS8250.  
YOLO-NAS is used to detect operators, tools, and equipment, while MediaPipe extracts human body keypoints. HRNet then performs pose analysis and maintenance SOP action recognition to verify whether each maintenance step follows the standard operating procedure.

All processing takes place on the edge device, ensuring better privacy and data protection

攝影機擷取即時影像串流，並由 QCS8250 在裝置端完成影像處理。  
利用 YOLO-NAS 偵測人員、工具及相關設備，再透過 MediaPipe 擷取人體姿態與關鍵點資訊，最後結合 HRNet 進行姿態分析與維修 SOP 動作辨識，判斷是否依照標準作業流程執行。

所有 AI 推論皆於 Edge Device 本地端完成，可降低延遲、提升即時性，並確保維修資料的隱私與安全。

<img src="QCS8250 維修SOP.assets/media/2.PNG" style="width:5.76806in;height:2.76319in" />

### Demo:



