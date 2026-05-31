# Pose Detection & Jump Performance Analysis

A computer vision project that uses MediaPipe Pose Landmarker and OpenCV to analyze vertical jump performance from video recordings.

The system extracts human body landmarks frame-by-frame, tracks movement patterns, calculates biomechanical metrics, and generates an annotated output video with pose landmarks.

## Features

* Human pose detection using MediaPipe
* Video-based jump analysis
* Automatic landmark extraction
* Jump height estimation
* Contact time calculation
* Flight time estimation
* Reactive Strength Index (RSI) computation
* Shoulder angle tracking
* Pose landmark visualization
* Annotated video generation

## Technologies Used

* Python
* MediaPipe
* OpenCV
* NumPy
* Pandas
* SciPy
* Matplotlib

## Project Workflow

1. Load video input.
2. Detect body landmarks using MediaPipe Pose Landmarker.
3. Extract hip, shoulder, knee, and ankle coordinates.
4. Track movement across frames.
5. Detect jump phases:

   * Crouch phase
   * Takeoff
   * Flight
   * Landing
6. Calculate performance metrics.
7. Generate visualizations and annotated output video.

## Performance Metrics

### Jump Height

Estimates vertical displacement during the jump using body landmark tracking and calibration factors.

### Contact Time

Measures the duration between the start of movement and takeoff.

### Flight Time

Calculates the airborne duration of the athlete.

### Reactive Strength Index (RSI)

RSI = Jump Height / Contact Time

Used to evaluate explosive athletic performance.

### Shoulder Angle Analysis

Tracks left and right shoulder angles throughout the movement to study upper-body mechanics.

## Installation

```bash
pip install mediapipe
pip install opencv-python
pip install numpy
pip install pandas
pip install scipy
pip install matplotlib
```

## Download MediaPipe Model

```bash
wget -O pose_landmarker.task \
https://storage.googleapis.com/mediapipe-models/pose_landmarker/pose_landmarker_heavy/float16/1/pose_landmarker_heavy.task
```

## Usage

Set the input video and athlete information:

```python
video_path = "video.MOV"
output_video_path = "output_video_with_landmarks.mp4"

H = 1.75
M = "male"
```

Run the analysis:

```python
jump_analyzer.process_video_for_landmarks()
jump_analyzer.analyze_jump_and_angles()
```

## Output

The system provides:

* Annotated pose video
* Jump height
* Contact time
* Flight time
* RSI score
* Shoulder angle graphs

## Example Applications

* Sports performance analysis
* Vertical jump testing
* Athlete monitoring
* Basketball training
* Volleyball performance assessment
* Biomechanics research
* Sports science projects

## Future Improvements

* Multi-athlete tracking
* Real-time webcam analysis
* Mobile deployment
* Knee angle analysis
* Force estimation
* Performance dashboard
* Machine learning-based movement classification

## License

MIT License

## Author

Developed for sports biomechanics and computer vision research using MediaPipe Pose Detection.
