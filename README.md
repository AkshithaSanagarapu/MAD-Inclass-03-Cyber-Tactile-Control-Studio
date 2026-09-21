# Cyber-Tactile Control Studio

This is my Flutter project for In-Class Activity 03 in Mobile App Development. The goal of this activity was to understand StatefulWidget, setState(), GestureDetector, and how small UI interactions can make an app feel more responsive.

For my customization, I created an AI Operations Control Center with four controls: Analyze, Deploy, Monitor, and Alert.

## Features

- Four customized controls: Analyze, Deploy, Monitor, and Alert
- Tactile buttons that visually press down when clicked
- Total tap counter
- Live status updates based on the selected control
- Power calibration slider
- Background warning color when power goes above 80%
- Light and dark mode
- Reusable TactileButton widget

## Controls

| Control | Action |
| --- | --- |
| Analyze | Activates data analysis |
| Deploy | Activates model deployment |
| Monitor | Activates system monitoring |
| Alert | Activates an incident alert |

## Flutter Concepts Used

- StatefulWidget
- setState()
- GestureDetector
- AnimatedContainer
- BoxShadow
- Slider
- Wrap
- Reusable custom widgets

## Tactile Button Interaction

Each TactileButton keeps track of its own `isPressed` state. `onTapDown` changes the button to its pressed state, while `onTapUp` returns it to normal and performs the button action. `onTapCancel` resets the button if the interaction is cancelled.

The button uses two BoxShadows with opposite offsets to create the raised 3D effect. When the button is pressed, the shadow offsets become smaller, which makes the button appear to move inward.

## Power Calibration

The power slider can be adjusted from 0% to 100%. I added visual feedback for the 80% threshold. When the power level goes above 80%, the background changes to a warning shade. Moving the slider back to 80% or below restores the normal background.

## Running the Project

To run the project:

```bash
flutter pub get
flutter run
```

To run it in Chrome:

```bash
flutter run -d chrome
```

## Course

Mobile App Development  
In-Class Activity 03: The Cyber-Tactile Control Studio