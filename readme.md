# Computer Vision - Action recognition

## Overall goal
The aim of this assignment is to classify actions in still images and videos using CNNs. The focus is on transfer learning, optical flow, and combining CNN outputs. The goal is not to achieve the best performance, but to pass the baseline accuracy scores for each task. Make informed choices and explain your choices and results in the report.

## Data
We will use two datasets:
1. Stanford 40: An image-based dataset for action recognition with 40 action classes and a total of 9532 images.
2. HMDB51: A dataset with short video clips of 51 action classes and a total of 6849 images.

## Classes Used
We will focus on the following 12 overlapping classes (HMDB51 - Stanford 40):
- applauding - clap hands
- climbing - climb
- drinking - drink
- jumping - jump
- pouring liquid - pour
- riding a bike - ride bike
- riding a horse - ride horse
- running - run
- shooting an arrow - shoot bow
- smoking - smoke
- throwing frisbee - throw
- waving hands - wave

## Tasks
We trained four different networks with different inputs and training strategies:
1. Stanford 40 - Frames: Train a CNN on the images in Stanford 40.
2. HMDB51 - Frames (transfer learning): Fine-tune a pretrained CNN on the middle frame of videos in HMDB51.
3. HMDB51 - Optical flow: Train a CNN on the optical flow of videos in HMDB51.
4. HMDB51 - Two-stream: Create a two-stream CNN with one stream for frames and one stream for optical flow. Fine-tune the network.

## Optical flow
Calculate the flow with a separate script and store the optical flow images in a separate directory.

## Baselines
The baseline accuracy score is ~8% due to 12 classes and stratification. Aim for scores well above 8% but don't expect too high accuracies.