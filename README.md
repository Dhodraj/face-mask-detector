# face-mask-detector

Checks a webcam feed and says whether the face inside the box on screen wears a mask. A small Keras CNN does the work, trained on pictures taken with the same webcam.

Built in June 2021.

## How it works

1. `Image_Generator.py` saves webcam crops into `data/`, one folder per class. Press 0, 1 or 2 to save a sample.
2. `training.ipynb` trains the CNN.
3. `roi.py` loads `model.h5` and labels every frame: Mask Detected, No Mask, or nothing.

## Run it

```bash
pip install tensorflow keras opencv-python imutils numpy
python roi.py
```

`roi.py` loads the model from a hard-coded Windows path. Point it at `model.h5` in this folder first. Press q to quit.
