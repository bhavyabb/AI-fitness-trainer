# AI-fitness-trainer

The **AI Fitness Trainer** is a Python-based application designed to assist users in monitoring and improving their exercise form using real-time pose detection. This project utilizes computer vision techniques with OpenCV and MediaPipe to track body movements during various exercises, providing feedback on performance and counting repetitions.

## Features

- **Real-time Pose Detection**: Utilizes MediaPipe to detect body landmarks and calculate angles for various exercises.
  
- **Exercise Tracking**: Supports multiple exercises including push-ups, squats, jumping jacks, sit-ups, and lunges, with real-time feedback on form and repetitions.

- **User Interface**: A simple graphical user interface (GUI) built with Tkinter for exercise selection and control.

- **Visual Feedback**: Provides visual cues for maintaining proper form and alignment during exercises.

## Requirements

To run this project, ensure you have the following installed:

- Python 3.x
- OpenCV
- NumPy
- MediaPipe
- Tkinter (usually included with Python installations)

You can install the required packages using pip:

```bash
pip install opencv-python numpy mediapipe
```

## File Structure

The project consists of two main files:

1. **`camera4.py`**: The main application file that handles video capture, pose detection, exercise logic, and the GUI.
  
2. **`PoseModule.py`**: A module that encapsulates the pose detection functionality using MediaPipe.

## Usage

### Running the Application

1. Ensure your webcam is connected and accessible.
  
2. Run the main application file:

   ```bash
   python camera4.py
   ```

3. Upon launching, a GUI will appear allowing you to select an exercise from the dropdown menu.

4. Click the "Start Exercise" button to begin tracking your selected exercise. The application will provide real-time feedback on your performance.

5. Press 'q' to quit the exercise session or use the "Quit" button in the GUI.

### Supported Exercises

The application currently supports the following exercises:

- Push-ups
- Squats
- Jumping Jacks
- Sit-ups
- Lunges

Each exercise has specific criteria for counting repetitions based on joint angles and body alignment.

## Functionality Detail

### Pose Detection

The `PoseModule.py` file contains a class `poseDetector` that implements methods for:
  
- Finding poses in images.
- Extracting landmark positions.
- Calculating angles between specified body points.

The angles are crucial for determining if the user is performing exercises correctly. 

### Exercise Logic

In `camera4.py`, each exercise has its own logic function (e.g., `push_up_logic`, `squats_logic`, etc.) that:

- Calculates necessary angles for proper form.
- Counts repetitions based on angle thresholds.
- Provides visual feedback on performance through progress bars and text messages displayed on the video feed.

### GUI Implementation

The Tkinter-based GUI allows users to:
  
- Select an exercise from a dropdown menu.
- Start or quit the exercise session easily.

## Contribution

Contributions are welcome! If you would like to contribute to this project, please fork the repository and submit a pull request with your changes. 

## License

This project is licensed under the MIT License - see the LICENSE file for details.
