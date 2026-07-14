✨ AeroCanvas AI

Draw in thin air. AeroCanvas AI turns your webcam into a touchless drawing canvas — no mouse, no stylus, no touchscreen. Just raise a finger and paint.

Built with MediaPipe Hands for real-time hand tracking, running entirely in your browser.


🎬 Features


Air Drawing — Raise your index finger to draw glowing neon strokes that follow your hand.
Hover / Navigation Mode — Raise index + middle fingers to move a cursor without drawing. Hover over a button for 1.5s to auto-click it — fully touchless UI control.
Eraser Mode — Open your palm fully to erase.
Live Hand Skeleton Overlay — See your tracked hand landmarks in real time (can be toggled off).
Custom Brush Colors & Sizes — 6 preset neon colors plus a full custom color picker, adjustable brush size (3–60px).
Undo / Redo / Clear — Full stroke history management.
Save Drawing — Export your artwork as an image.
Camera Feed Toggle — Show or hide the webcam background while keeping your drawing visible.
Performance-Optimized Rendering — Uses an offscreen "baked" canvas so drawing stays fast (O(1) per frame) even with hundreds of strokes, plus a non-blocking camera/inference loop tuned for minimal input lag.
Friendly Camera Error Handling — Clear troubleshooting tips if the camera can't be accessed (in use by another app, permission denied, not found, etc.).


✋ Gesture Guide

GestureModeWhat it does☝️ Index finger onlyDrawDraws lines in the air✌️ Index + Middle fingersHover / NavigateMoves cursor only; hover 1.5s over a button to click it🖐️ Open palmEraserErases strokes under your hand

🚀 Getting Started

Requirements


Python 3 (for the local server)
A webcam
A modern browser (Chrome recommended) with camera permissions allowed


Run it

bashpython run.py

This starts a local server at http://localhost:8000 and automatically opens it in your default browser. Allow camera access when prompted, and start drawing!


Keep the terminal window open while using the app. Press Ctrl+C to stop the server.



Alternative: manual setup

If you'd rather not use run.py, serve the project folder with any static file server (e.g. python -m http.server 8000) and open http://localhost:8000 in your browser. index.html can't simply be opened as a file:// URL because camera access and the MediaPipe scripts require an HTTP context.

🗂️ Project Structure

├── index.html   # App layout, controls panel, gesture guide
├── style.css    # Glassmorphic neon UI styling
├── app.js       # Hand tracking, gesture logic, drawing engine
└── run.py       # Local server launcher

🛠️ Tech Stack


MediaPipe Hands — real-time hand landmark detection
Vanilla JavaScript — no frameworks, direct Canvas 2D API for drawing
HTML5 Canvas — layered canvases for painting, live tracking overlay, and offscreen stroke baking
CSS3 — glassmorphism + neon glow aesthetic
Python (http.server) — zero-dependency local dev server


💡 Tips


Good, even lighting on your hand improves tracking accuracy.
Keep your hand within the camera frame for continuous tracking.
If the camera fails to start, close other apps (Zoom, Teams, Skype) that might be using it, then click Try Again.



Made by Asim Raza
