# Work_Attendance_Controller_OpenCV

Track employee attendance with ease using facial recognition and Python. This project provides a simple yet effective solution for managing work hours through automated face recognition.

## Table of Contents
- [Features](#features)
- [How It Works](#how-it-works)
- [Technology Stack](#technology-stack)
- [Requirements](#requirements)
- [Installation](#installation)
- [Configuration](#configuration)
- [Quick Start](#quick-start)
- [Usage](#usage)
- [Project Structure](#project-structure)

## Features
### Face Recognition Integration
- **What it does:** Utilizes OpenCV for real-time face detection and recognition.
- **Why it exists:** Ensures accurate identification of employees, reducing the risk of unauthorized access.

### Simple Configuration
- **What it does:** Easy setup with minimal configuration required.
- **Why it exists:** Facilitates quick deployment and reduces the learning curve for users.

## How It Works
The application captures video from a webcam, detects faces in real-time, and compares them against a database of authorized employees. If a match is found, the system records the attendance.

```plaintext
+-------------------+
|  Webcam           |
|                   |
|  +---------------+ |
|  | Face Detection| |
|  +---------------+ |
|                   |
|  +---------------+ |
|  | Recognition   | |
|  +---------------+ |
|                   |
|  +---------------+ |
|  | Attendance    | |
|  +---------------+ |
+-------------------+
```

## Technology Stack
| Technology | Purpose |
|------------|---------|
| OpenCV     | Face detection and recognition. |
| Python     | Main programming language. |

## Requirements
- Python 3.x
- OpenCV library

## Installation
To install the required dependencies, run:

```bash
pip install opencv-python
```

## Configuration
No additional configuration is required beyond installing the dependencies.

## Quick Start
1. Clone the repository:
   ```bash
   git clone https://github.com/PartORG/Work_Attendance_Controller_OpenCV.git
   cd Work_Attendance_Controller_OpenCV
   ```
2. Run the application:
   ```bash
   python main.py
   ```

## Usage
The application will start capturing video from your webcam and prompt you to press 'q' to exit.

```python
# main.py
import cv2

def main():
    cap = cv2.VideoCapture(0)
    while True:
        ret, frame = cap.read()
        if not ret:
            break
        cv2.imshow('Work Attendance', frame)
        if cv2.waitKey(1) & 0xFF == ord('q'):
            break
    cap.release()
    cv2.destroyAllWindows()

if __name__ == "__main__":
    main()
```

## Project Structure

```plaintext
.
├── .gitignore
├── Employees/
│   ├── Brad Pitt.jpg
│   ├── Freddy Miller.jpg
│   ├── Ievgen Perederieiev.jpg
│   ├── Justin Conor.jpg
│   ├── Kim Frednong.jpg
│   └── Sam Herriot.jpg
├── README.md
├── main.py
└── work_attendance.py
```

## Development

This project is open for contributions. Feel free to submit issues or pull requests.

## License

This project is not licensed. Use it at your own risk.