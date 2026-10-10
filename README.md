# Handschrifterkennung
# Handwritten Character Recognition System (MATLAB)

An interactive MATLAB-based system for offline handwritten character and digit recognition utilizing **Feed-Forward Neural Networks (Multi-Layer Perceptron - MLP)** trained via backpropagation, supported by a custom Graphical User Interface (GUI).

## Project Overview
This project was developed as a graduation/academic project at **Tartous University, Faculty of Information Technology Engineering**. It processes scanned handwritten inputs, performs image pre-processing, extracts structural and statistical features, and classifies the characters using a trained neural network.

---

## Key Features & Architecture

1. **Image Pre-processing:**
   - Conversion from RGB to Grayscale.
   - Image Binarization using thresholding techniques.
   - Edge Detection (using Laplacian method with zero-crossing).
   - Morphological operations (Dilation and Hole Filling).

2. **Feature Extraction & Object Location:**
   - Manual and automated object cropping and bounding box extraction (`regionprops`).
   - Resizing characters into normalized bitmap representations (`7x5` and `70x50` grids).

3. **Neural Network Classification (Backend):**
   - Implemented a **Feed-Forward Neural Network** trained with Gradient Descent Backpropagation with Adaptive Learning Rate (`traingdx`)[cite: 16].
   - Uses logarithmic sigmoid transfer functions (`logsig`).

4. **Graphical User Interface (GUI):**
   - Custom-built MATLAB GUI (`charGUI` / `charGUI2`) allowing users to load images, crop regions of interest, run pre-processing, extract features, and display recognized characters interactively.

---

## Project Structure
- `charGUI.m` / `charGUI2.m`: Main MATLAB GUI scripts for user interaction and workflow execution.
- `edu_createnn.m`: Neural network creation, configuration, and training script.
- `edu_imgpreprocess.m`: Handles image binarization, edge detection, and morphological filtering.
- `edu_imgresize.m`: Feature extraction and grid normalization script.

---

## How to Run
1. Open **MATLAB** and set the project directory as your current workspace.
2. Run the GUI script by typing in the MATLAB Command Window:
   ```matlab
   charGUI2
