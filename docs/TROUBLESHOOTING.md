# Troubleshooting

## `ModuleNotFoundError: No module named 'ultralytics'`
Activate the project virtual environment and install the dependencies from `requirements.txt`.

```bash
python -m pip install -r requirements.txt
```

## Camera does not open
- Check that the webcam is available.
- Close other applications using the camera.
- Verify that OpenCV can access the selected camera index.

## Alarm audio is not playing
- Confirm the `.mp3` files are present in the project directory.
- Check that the audio device is available.
- Reinstall the project dependencies if the pygame import fails.
