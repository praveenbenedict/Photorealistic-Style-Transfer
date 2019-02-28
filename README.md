# Photorealistic-Style-Transfer

## Objective
Based on the Yagudin et. al's pytorch implementation of the Deep Photo Style Transfer paper ( Luan et. al ), we aim to explore new applications and modifications of photo styletransfer. We are mainly concerned with speeding up the process of styletransfer which is extremely time consuming as of now and with exploring how different styles can be combined onto a single content image.

## Roles
Amaury : setting up a new database of images based on a Google image scrapper

Victor : setting up a framework in which the code can easily be edited, run on specific experiments and monitored for performances

Nicolas : Looking for changes which could improve the time needed to process an image. 

## Changes

CUDA support was added in several functions ( image_preprocessing.image_to_tensor and image_preprocessing.tensor_to_image)

## Ideas for improvement

When running the script, I noticed that the regularization loss was often negative and was very unstable.
Example :

step  200: S: 89.747 C: 4.231 R:-5559.885

step  250: S: 88.981 C: 5.352 R:1647.456

step  300: S: 89.943 C: 5.703 R:-3204.946

step  350: S: 89.955 C: 13.522 R:-4951.400

step  400: S: 97.520 C: 7.561 R:-3702.983

step  450: S: 229.646 C: 46.452 R:21189.082

step  500: S: 229.500 C: 43.207 R:19783.462

We should investigate into this behavior


## Credits
The entire code structure is cloned from : https://github.com/yagudin/PyTorch-deep-photo-styletransfer
