

## Introduction
This is an adapted version of original mmaction2 and with reference to this repo[GitHub Pages]([https://pages.github.com/](https://github.com/Whiffe/mmaction2_YF)).
Original version by default use faster rcnn and I try to use YOLOv3 for the action recognition due to faster classification.
The result can be found on demo folder. Video demoOut.MP4 is the output of a sample video showing 2 people doing arm wrestling. The model is able to locate the people and produce the prediction of actions. However, the prediction is not very accurate. Suspect the activity arm wrestling is not inside the pretrained model.

## For testing
Please run the following code with your own video.mp4
```
python demo/demo_spatiotemporal_det.py --config configs/detection/ava/slowfast_kinetics_pretrained_r50_8x8x1_20e_ava_rgb.py --checkpoint Checkpionts/mmaction/slowfast_r50_8x8x1_256e_kinetics400_rgb_20200716-73547d2b.pth --det-config demo/yolov3_d53_320_273e_coco.py  --det-checkpoint Checkpionts/mmdetection/yolov3_d53_320_273e_coco-421362b6.pth   --video /user-data/mmactionVideo/video/your_input_video_name.mp4  --out-filename demo/your_output_name.mp4  --det-score-thr 0.9 --action-score-thr 0.5 --output-stepsize 4  --output-fps 6
```
MMAction2 is an open-source toolbox for video understanding based on PyTorch.
It is a part of the [OpenMMLab](http://openmmlab.org/) project.



