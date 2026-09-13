# System Architecture

```text
Webcam
  ↓
OpenCV Frame Capture
  ↓
Face Mesh + Eye Analysis ──→ Sleepiness Warning
  ↓
YOLO Object Detection ─────→ Phone Warning
  ↓
Priority-based Audio Alerts
  ↓
On-screen Monitoring Output
```

The monitor combines face/eye analysis with object detection so different study-distraction signals can be handled in one workflow.
