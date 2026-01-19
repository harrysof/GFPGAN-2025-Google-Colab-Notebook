# GFPGAN-2025 Google Colab Notebook

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/harrysof/GFPGAN-2025-Google-Colab-Notebook)

Updated — Colab-ready Jupyter notebook(s) for running GFPGAN-based face restoration and enhancement in Google Colab.

## Overview
This repository contains one or more Google Colab notebooks that set up and run GFPGAN (Generative Facial Prior GAN) to restore and enhance faces in images. The notebook automates dependency installation, downloads required model weights, and provides a simple UI for uploading images, running restoration, and downloading results.

GFPGAN is ideal for face restoration, removing artifacts, and improving fidelity of low-quality face images.

Official GFPGAN repo: https://github.com/TencentARC/GFPGAN

## Features
- One-click Colab setup to run GFPGAN
- Automatic download/install of dependencies and model weights (as configured in the notebook)
- Simple interface to upload images and restore faces
- Options for upscaling and blending restored faces with original images
- Example inputs and outputs for quick testing

## Quickstart (Open in Colab)
1. Click the "Open in Colab" badge above.
2. In Colab: Runtime → Change runtime type → select "GPU" (recommended) and Hardware accelerator = GPU.
3. Run the first cell to install dependencies and download model weights.
4. Upload your image(s) using the notebook upload cell or mount Google Drive.
5. Run the inference cell(s) to restore faces.
6. Download or save results to your Drive.

The notebook includes inline instructions and example usage cells — run the cells sequentially.

## Requirements
- Google Colab (recommended) — GPU runtime
- If running locally:
  - Python 3.8+ (match PyTorch compatibility)
  - CUDA-capable GPU (recommended for reasonable performance)
  - Dependencies (installed by the notebook or via pip): torch, torchvision, basicsr, facexlib, gfpgan, opencv-python, numpy, pillow, matplotlib, tqdm
  - Exact dependency installation commands are provided in the notebook; run those cells or the included setup script.

## Running Locally (outline)
1. Clone the repository:
   git clone https://github.com/harrysof/GFPGAN-2025-Google-Colab-Notebook.git
2. Create and activate a virtual environment:
   python -m venv venv
   source venv/bin/activate  # Linux / macOS
   venv\Scripts\activate     # Windows
3. Install dependencies (example):
   pip install torch torchvision --extra-index-url https://download.pytorch.org/whl/cu117
   pip install basicsr facexlib gfpgan opencv-python pillow matplotlib tqdm
4. Download GFPGAN weights (see notebook or GFPGAN releases).
5. Run the notebook with Jupyter or convert example cells to scripts as needed.

Note: local installation and GPU configuration details depend on your system and chosen CUDA/cuDNN versions.

## Notebook structure (typical)
- Setup: install Python packages and download weights
- Configuration: set restore/upscale parameters
- Input: upload images or mount Google Drive
- Inference: run GFPGAN restoration
- Output: preview and save restored images
- Advanced: tuning options and batch processing

## Model weights
The notebook is configured to download GFPGAN model weights automatically (or includes instructions to place them in a weights folder). If the notebook does not automatically fetch weights, download them from the official GFPGAN releases page:
https://github.com/TencentARC/GFPGAN/releases

Place the weights in the path expected by the notebook (check the "weights" path variable in the setup cell).

## Tips
- Use a GPU runtime in Colab for performance. TPU is not supported for GFPGAN.
- For high-resolution images, increase available memory or process in smaller tiles.
- If you see artifacts, try different restoration strengths or the background/face fusion options.
- Save outputs to Google Drive if processing many images.

## Troubleshooting
- Dependency or import errors: re-run the setup cell to ensure packages installed correctly; check for PyTorch/CUDA compatibility.
- Weight download failed: manually download weights from the release page and upload to the notebook or Drive.
- OOM (out-of-memory) errors: switch to a smaller input image size or use a lower batch size; use Colab Pro for more RAM/GPU memory.

## Contributing
- Found an issue or improvement? Open an issue or submit a pull request.
- If you add new notebooks or examples, please document usage and add reproducible setup steps.

## License
This repository currently contains no explicit license file. If you want others to reuse or contribute, add a LICENSE (e.g., MIT) to clarify terms. Note: GFPGAN and associated model weights are subject to their original license—check the upstream project's license before commercial use.

## Acknowledgements
- GFPGAN authors and contributors (Tencent ARC)
- The broader open-source community for image restoration libraries (basicsr, facexlib, etc.)

## Contact
Repository owner: harrysof — https://github.com/harrysof

If you want any specific formatting, additional badges, or a LICENSE file added, tell me which license you'd like and whether you want a sample usage section expanded with concrete example commands or notebook cell contents.
