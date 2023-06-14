
# Catch the Eatable Object Game

This project is a simple game where the player uses their facial movements to catch eatable objects that fall from the top of the screen. The game utilizes facial recognition and tracking to detect the player's movements and determine if they successfully catch the objects or not.

## Methodology

The game utilizes the following steps to create the interactive experience:

1. Capture Webcam: The project uses OpenCV to capture the webcam feed as video input.

2. Face Mesh Detection: The `FaceMeshModule` from the `cvzone` library is used to detect and track facial landmarks in real-time. This provides the necessary information for tracking the player's facial movements.

3. Object Import: The project imports images of eatable and non-eatable objects from specified folders. These objects will be displayed and fall from the top of the screen.

4. Object Movement: The objects are displayed on the screen, and their positions are updated to create the falling effect. The position of the objects is tracked using the `pos` variable, and the speed of falling is controlled by the `speed` variable.

5. Facial Movements: The project tracks specific facial landmarks, such as the position of the lips, to determine the player's facial movements. The distance between the upper and lower lips is calculated to determine if the player's mouth is open or closed.

6. Object Interaction: The project calculates the distance between the falling object and the player's mouth position. If the object is within a certain distance and the player's mouth is open, it is considered a successful catch. Otherwise, it results in a game over.

7. Game Over and Score: If the player fails to catch an object, the game over state is triggered. The player's score is displayed on the screen, showing the number of successfully caught objects.

8. Game Reset: The player can reset the game by pressing the 'r' key. This resets the game variables and starts a new round.

## Requirements

To run this project, you need the following requirements:

- Python 3.6 or above
- OpenCV library
- cvzone library
- Webcam or camera connected to your system

## Installation

1. Clone the repository to your local machine:
   ```
   git clone <repository_url>
   ```

2. Install the required libraries using pip:
   ```
   pip install opencv-python
   pip install cvzone
   ```

## Usage

1. Navigate to the project directory.

2. Run the Python script:
   ```
   python catch_eatable_object_game.py
   ```

3. The webcam feed will open, and you can start playing the game. Use your facial movements to catch the falling objects.

4. Press the 'r' key to reset the game and start a new round.
