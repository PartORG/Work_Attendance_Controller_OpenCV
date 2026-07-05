# Work_Attendance_Controller_OpenCV

Track employee attendance with ease using face recognition technology. This simple Python app leverages OpenCV to identify faces and log work hours.

[![Python](https://img.shields.io/badge/python-3.x-blue.svg)] [![License](https://img.shields.io/badge/license-MIT-green.svg)] [![Package Manager](https://img.shields.io/badge/package-manager-pip-yellow.svg)] [![Framework](https://img.shields.io/badge/framework-OpenCV-red.svg)]

## Introduction

Work_Attendance_Controller_OpenCV is a Python application designed to streamline the process of employee attendance tracking. By utilizing face recognition, this app provides an efficient and accurate way to log when employees enter and leave the workplace.

The primary workflow involves loading pre-defined images of employees into the system. When an employee enters the premises, the app captures their image and compares it against the stored images to identify them. Once identified, the app logs the employee's attendance.

This solution is ideal for small businesses or teams that want a simple yet effective way to manage work hours without the need for complex systems.

## Features

- **Face Recognition**: Accurately identifies employees using pre-loaded images.
- **Real-Time Attendance Logging**: Logs entry and exit times in real-time.
- **User-Friendly Interface**: Simple Python script with minimal setup required.

## How It Works

The app is built on top of the OpenCV library, which provides powerful computer vision capabilities. The workflow involves the following steps:

1. Load pre-defined employee images into the system.
2. Capture an image when an employee enters the premises.
3. Compare the captured image against the stored images to identify the employee.
4. Log the attendance based on the identified employee.

Below is a simplified ASCII diagram illustrating the app's workflow:

```
+-------------------+
| Load Employee Images|
+---------+---------+
          |
          v
+---------+---------+
| Capture Image   |
+---------+---------+
          |
          v
+---------+---------+
| Compare with Stored Images |
+---------+---------+
          |
          v
+---------+---------+
| Log Attendance  |
+-------------------+
```

## Technology Stack

| Technology | Purpose |
|------------|---------|
| Python     | Main programming language for the application. |
| OpenCV     | Library used for face recognition and image processing. |

## Requirements

- Python 3.x
- OpenCV library

## Installation

To install the required dependencies, run the following command:

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

The `main.py` script is the entry point for the application. It loads employee images and captures images from the camera to identify employees.

Here are some example commands:

```bash
# Load employee images
python work_attendance.py load_images

# Capture an image and log attendance
python main.py capture_and_log
```

## Project Structure

```
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

- `Employees/`: Directory containing pre-defined employee images.
- `main.py`: Entry point for the application.
- `work_attendance.py`: Script for loading and processing employee images.

## Development

The development workflow involves:

1. Writing Python scripts to handle face recognition and attendance logging.
2. Testing the application with various scenarios.
3. Refining the code based on feedback.

## Limitations

- The app currently only supports pre-defined employee images.
- Real-time video capture is not implemented, so manual image capture is required for now.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.