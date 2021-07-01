# Tutorial

## Modify yolov5 source code
- Download the file `model.py` from this [link](https://drive.google.com/file/d/13S4Zjf7PpfHNynpAkp-po6RnatE4Y-mw/view?usp=sharing).
- Replace `model.py` in folder `yolov5/models/` with the one you've just downloaded.

## Create virtualenv
```
python3 -m venv furniture_detection
source furniture_detection/bin/activate
pip install -qr requirements.txt
```
## Install packages
```
cd yolov5
pip install -qr requirements.txt
```
## Prepare your dataset
- You should break down your data into 3 seperate folders `train`, `valid`, and `test`
- Each folder contains 2 folders namely `images` and `labels`:
  - `images/` contains .jpg image files.
  - `labels/` contains corresponding .txt label files.
- The .txt label file should be in YOLO format as below:
 ```
  Label_ID_1 X_CENTER_NORM Y_CENTER_NORM WIDTH_NORM HEIGHT_NORM
  Label_ID_2 X_CENTER_NORM Y_CENTER_NORM WIDTH_NORM HEIGHT_NORM
 ```
 with 
 ```
  X_CENTER_NORM = X_CENTER_ABS/IMAGE_WIDTH
  Y_CENTER_NORM = Y_CENTER_ABS/IMAGE_HEIGHT
  WIDTH_NORM = WIDTH_OF_LABEL_ABS/IMAGE_WIDTH
  HEIGHT_NORM = HEIGHT_OF_LABEL_ABS/IMAGE_HEIGHT
 ```
- Note: The image and its corresponding label must have the same name, i.e 'img1.jpg' has 'img1.txt' as its corresponding label.
- Modify the attributes `nc` and `names` in `data.yaml` file to match your dataset description

## Follow the codes in the notebook (.ipynb file) to train your model
The notebook is used to demonstrate the training process more efficiently, please follow the instructions in the notebook to train your model without facing any unwanted issues.
