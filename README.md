
# 🎨 Virtual Painter using OpenCV

This project implements an Virtual Painter in Python using OpenCV.  
By holding a colored marker (e.g., a blue cap, red object, etc.) in front of your webcam, you can draw in the air, and the strokes will appear on the screen in real time.

---

## ✨ Features
- Real-time tracking of a colored object using **HSV color space**.
- Adjustable HSV values via trackbars for accurate marker detection.
- Virtual drawing canvas with **multiple colors** (Blue, Green, Red, Yellow).
- **Clear All** button to erase the canvas instantly.
- Separate drawing window (`Paint`) that keeps track of your sketches.
- Save and replay functionality can be added easily.

---

## 🛠️ Requirements
- Python 3.x  
- OpenCV  
- NumPy  

Install dependencies with:
```bash
pip install opencv-python numpy
````

---

## 📷 How it Works

1. The webcam captures your video feed.
2. A color object (marker) is detected using **HSV color thresholds**.
3. The detected marker’s position is stored and drawn on both:

   * The live webcam feed (`Tracking` window).
   * A separate white canvas (`Paint` window).
4. You can switch drawing colors or clear the canvas by moving the marker into the button area at the top of the frame.

---

## 🎨 Controls

* **Top buttons**:

  * `CLEAR ALL` → Erase the canvas.
  * `BLUE`, `GREEN`, `RED`, `YELLOW` → Change drawing color.
* **q key** → Quit the application.

---

## 📂 Project Structure

* `Air_canvas.py` → Main script to run the project.

---

## 🚀 Run the Project

```bash
python Air_canvas.py
```

---

## ⚙️ Customize

* **Change marker color**:
  Use the trackbars (`Color detectors` window) to adjust HSV values for your marker.

* **Change colors in palette**:
  Modify this part of the code:

  ```python
  colors = [(255, 0, 0),   # Blue
            (0, 255, 0),   # Green
            (0, 0, 255),   # Red
            (0, 255, 255)] # Yellow
  ```

---

## 📌 Notes

* Ensure good lighting conditions for stable detection.
* Use a bright-colored object that doesn’t match your background.
* If detection is unstable, fine-tune the **HSV values** with the trackbars.

---

## 📜 License

This project is open-source and free to use for learning and development.

