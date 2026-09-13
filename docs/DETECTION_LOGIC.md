# Detection Logic

The application combines multiple signals:

- Face/eye measurements are used to identify prolonged sleepy-eye patterns.
- Face visibility is monitored so missing or covered faces can trigger a warning.
- YOLO-based object detection checks for a mobile phone with a confidence threshold.
- Audio alerts use a priority order so important warnings are not silently ignored.

Thresholds are implementation parameters and should be tuned with real testing rather than assumed to be universally accurate.
