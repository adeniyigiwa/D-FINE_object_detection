# D-FINE Object Detection Demo

**D-FINE** (Fine-grained Distribution Refinement) is a state-of-the-art real-time object detection model built on top of DETR. This repository provides a Colab-ready setup and a minimal Gradio web application to showcase D-FINE’s high-precision detections at real-time speeds.

---

## Table of Contents

1. [Features](#features)
2. [Prerequisites](#prerequisites)
3. [Google Colab](#google-colab)
4. [License](#license)
5. [Acknowledgements](#acknowledgements)

---

## Features

* **Fine-grained Distribution Refinement (FDR):** Iterative, probabilistic bounding-box edge regression for precise localization.
* **Global Optimal Localization Self-Distillation (GO-LSD):** Self-distillation mechanism that transfers refined localization signals across decoder layers.
* **Colab-Ready:** One-click setup instructions for Google Colab.
* **Interactive Gradio App:** Web-based interface for uploading images and visualizing detections instantly.

---

## Prerequisites

* Python 3.8 or later
* GPU with CUDA support (for Colab, ensure GPU runtime)

---

## Google Colab

1. Open the [demo notebook](https://github.com/adeniyigiwa/D-FINE_object_detection/blob/main/D_Fine.ipynb).
2. Run the setup cell to install the latest Transformers and other dependencies:

   ```bash
   !pip install --upgrade git+https://github.com/huggingface/transformers.git  
   !pip install torch torchvision --extra-index-url https://download.pytorch.org/whl/cu118  
   !pip install pillow opencv-python gradio
   ```
3. Switch the runtime to **GPU**: *Edit → Notebook settings → Hardware accelerator → GPU*.
4. Run all cells to:

   * Load the D-FINE model from Hugging Face.
   * Perform inference on a sample image.
   * Launch the Gradio app directly within Colab (with `share=True`).

---

## License

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.

---

## Acknowledgements

* [D-FINE Paper (arXiv:2410.13842)](https://arxiv.org/abs/2410.13842)
* [Hugging Face Transformers](https://github.com/huggingface/transformers)
* [Gradio](https://gradio.app)
