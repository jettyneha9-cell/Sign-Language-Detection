# Sign-Language-Detection
It's a full end to end DETR object detection pipeline, in this video its fine tuned for detecting signs but it could definitely be repurposed for other object detection tasks. It covers:  
⚡️ Detections using my pre-trained transformer
💾 Collecting custom data for you to train your own
🏋🏽‍♀️ Fine tuning, with or without pre-trained weights


Setup 
Install UV - pip install uv
Install all the dependencies uv sync

Collecting images
Update classes in src/utils/collect_images.py
Run the script uv run src/utils/collect_images.py

Labelling them
Make sure label-studio is installed uv pip list | grep label-studio
Run the labelling tool uv run label-studio

Create new project, setup
Labelling shortcuts CTRL + Enter submit, enter number per label
Training 🦾
Create a checkpoints folder mkdir checkpoints
Run the training pipeline uv run src/train.py
Running 🚀
To test on your test set, update the checkpoint parameter in test.py then run uv run src/test.py
To run in real time, update the checkpoint parameter in realtime.py then run uv run src/realtime.py
N.B. you might need need to update your camera parameter in cv2.VideoCapture() to get the right webcam for your machine.
