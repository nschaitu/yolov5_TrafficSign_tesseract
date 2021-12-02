### based code: https://github.com/ultralytics/yolov5

After unzip yolov5_TrafficSign_tesseract,zip file, 

change directory 
> cd yolov5_TrafficSign_tesseract

Install dependency
> pip install -r requirements.txt

## Training
follow this jupyter notebook: YOLOv5_TrafficSign_training.ipynb 

After successfully completing training, copy weight file from runs/train/{exp_name}/weights/best.pt to saved_weights

## inference
> python detect_tesseract.py --weights saved_weights/best.pt --img 1260 --use-tesseract --view-img --save-crop --source data/test_images/test1.png

For more info. check --help tag
> python detect_tesseract.py --help

Note: --source--source 0  # webcam
                          img.jpg  # image 
                          vid.mp4  # video
                          path/  # directory
                          path/*.jpg  # glob
                          'https://youtu.be/Zgi9g1ksQHc'  # YouTube
                          'rtsp://example.com/media.mp4'  # RTSP, RTMP, HTTP stream