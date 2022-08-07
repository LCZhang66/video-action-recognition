<div align="center">
  <img src="https://github.com/open-mmlab/mmaction2/raw/master/resources/mmaction2_logo.png" width="500"/>
</div>

## Introduction
This is an adapted version of original mmaction2. Original version by default use faster rcnn and I try to use YOLOv3 for the action recognition due to faster classification.
The result can be found on demo folder. Video demoOut.MP4 is the output of a sample video showing 2 people doing arm wrestling. The model is able to locate the people and produce the prediction of actions. However, the prediction is not very accurate. Suspect the activity arm wrestling is not inside the pretrained model.

## For testing
Please run the following code with your own video.mp4

python demo/demo_spatiotemporal_det.py --config configs/detection/ava/slowfast_kinetics_pretrained_r50_8x8x1_20e_ava_rgb.py --checkpoint Checkpionts/mmaction/slowfast_r50_8x8x1_256e_kinetics400_rgb_20200716-73547d2b.pth --det-config demo/yolov3_d53_320_273e_coco.py  --det-checkpoint Checkpionts/mmdetection/yolov3_d53_320_273e_coco-421362b6.pth   --video /user-data/mmactionVideo/video/your_input_video_name.mp4  --out-filename demo/your_output_name.mp4  --det-score-thr 0.9 --action-score-thr 0.5 --output-stepsize 4  --output-fps 6

MMAction2 is an open-source toolbox for video understanding based on PyTorch.
It is a part of the [OpenMMLab](http://openmmlab.org/) project.

The master branch works with **PyTorch 1.3+**.

<div align="center">
  <div style="float:left;margin-right:10px;">
  <img src="https://github.com/open-mmlab/mmaction2/raw/master/resources/mmaction2_overview.gif" width="380px"><br>
    <p style="font-size:1.5vw;">Action Recognition Results on Kinetics-400</p>
  </div>
  <div style="float:right;margin-right:0px;">
  <img src="https://user-images.githubusercontent.com/34324155/123989146-2ecae680-d9fb-11eb-916b-b9db5563a9e5.gif" width="380px"><br>
    <p style="font-size:1.5vw;">Skeleton-base Action Recognition Results on NTU-RGB+D-120</p>
  </div>
</div>
<div align="center">
  <img src="https://github.com/open-mmlab/mmaction2/raw/master/resources/spatio-temporal-det.gif" width="800px"/><br>
    <p style="font-size:1.5vw;">Spatio-Temporal Action Detection Results on AVA-2.1</p>
</div>

