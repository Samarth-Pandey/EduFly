# EduFly — Proton Gesture & Virtual Paint

Lightweight demo that combines a voice assistant (Proton), gesture-based system control, and an air-canvas (virtual paint) using MediaPipe, OpenCV and Eel.

## Quick overview
- Voice UI + web chat: [`app.ChatBot`](app.py), UI served from [web/index.html](web/index.html).  
- Voice assistant & command dispatcher: [`Proton.respond`](Proton.py), [`Proton.record_audio`](Proton.py), [`Proton.reply`](Proton.py).  
- Gesture controller (mouse, click, pinch controls, volume/brightness): [`Gesture_Controller.GestureController`](Gesture_Controller.py), including [`Gesture_Controller.Controller`](Gesture_Controller.py), [`Gesture_Controller.HandRecog`](Gesture_Controller.py), [`Gesture_Controller.Gest`](Gesture_Controller.py), [`Gesture_Controller.HLabel`](Gesture_Controller.py).  
- Virtual paint (air canvas): [`Paint.virtualpaint`](Paint.py) (uses [`track_hands.handDetector`](track_hands.py)).  
- Lightweight virtual-paint helper (alternative/simple VM paint controller): [`format_for_paint.VirtualPaintController`](format_for_paint.py).  
- Browser frontend JS helpers: [`web.js.main.addUserMsg`](web/js/main.js), [`web.js.main.addAppMsg`](web/js/main.js), [`web.js.main.getUserInput`](web/js/main.js).

## Requirements
Install Python 3.7+ and the required packages (example):
```sh
pip install opencv-python mediapipe numpy pyttsx3 SpeechRecognition pynput pyautogui eel pycaw comtypes screen-brightness-control wikipedia