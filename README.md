# Handsfree Mouse Control

A Python-based application that uses MediaPipe Face Mesh to control the mouse cursor with eye tracking and blink gestures.

## Project Overview

This repository includes a single script, `i.py`, which captures webcam video, detects facial landmarks using MediaPipe, and maps eye gaze to screen coordinates. A blink is interpreted as a left click, enabling hands-free mouse control.

## Features

- Real-time webcam capture using OpenCV
- Face mesh and iris landmark detection with MediaPipe
- Cursor movement mapped from eye position to screen coordinates
- Blink detection for click actions using eye landmark distance
- Simple setup with Python and standard libraries

## Requirements

- Python 3.8 or newer
- A webcam
- Windows (recommended for best `pyautogui` compatibility)

## Dependencies

Install the required Python packages:

```powershell
python -m pip install opencv-python mediapipe pyautogui
```

If you prefer using a virtual environment:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install opencv-python mediapipe pyautogui
```

## Usage

Run the script from the project folder:

```powershell
python i.py
```

Then position your face in front of the webcam. The cursor should follow the detected iris position, and a quick blink will trigger a click.

## File Structure

- `i.py` — main application script
- `README.md` — project documentation

## Notes and Recommendations

- Ensure good lighting and a clear webcam view for stable landmark detection.
- Keep the webcam centered in front of your face to improve cursor tracking.
- If the cursor is too sensitive, adjust the landmark mapping logic in `i.py`.

## Troubleshooting

- If the webcam is not detected, make sure no other application is using it.
- If `mediapipe` installation fails, ensure your Python version is supported and try upgrading `pip`.
- `pyautogui` may require additional permissions on some systems.

## License

This project is released under the MIT License.
