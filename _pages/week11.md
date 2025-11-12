---
layout: page
title: Week 11
permalink: /week11/
---

## Week 11 Activities

- ml5.js workshop
- Sound
- Final project discussion

---

## Class notes

Examples from class:

- [BodyPose Orb](https://craigfahner.github.io/CC2025-cef9489/ml5-pose-bubble/) - [code](https://github.com/craigfahner/CC2025-cef9489/tree/main/ml5-pose-bubble)
- [HandPose pinch detector](https://craigfahner.github.io/CC2025-cef9489/ml5-handpose) - [code](https://github.com/craigfahner/CC2025-cef9489/tree/main/ml5-handpose)
- [FaceMesh mask](https://craigfahner.github.io/CC2025-cef9489/ml5-facemesh) - [code](https://github.com/craigfahner/CC2025-cef9489/tree/main/ml5-facemesh)

# ml5.js workshop
ml5.js is a p5.js library that provides access to TensorFlow.js machine learning models that do things like detect the positions of hands, facial features and poses from images and videos.

To install ml5.js, first create a new p5.js sketch from your template folder. Then add the following line to the `<head>` portion of your sketch's index.html file:

    <script src="https://unpkg.com/ml5@1/dist/ml5.min.js"></script>

Today we will be working off of the following examples:

ML5 models:
- [BodyPose](https://docs.ml5js.org/#/reference/bodypose): Detects "skeleton" – arms, legs, torso, head positions
	-   [BodyPose MoveNet Keypoints](https://editor.p5js.org/ml5/sketches/hMN9GdrO3): Draw the keypoints of the detected body using MoveNet model.
	-  [Pose Estimation with ml5.js](https://thecodingtrain.com/tracks/ml5js-beginners-guide/ml5/7-bodypose/pose-detection)  by The Coding Train (video tutorial)
- [HandPose](https://docs.ml5js.org/#/reference/handpose): detects positions of hand, palm and fingers
	- [HandPose Keypoints](https://editor.p5js.org/ml5/sketches/QGH3dwJ1A): Draw the keypoints of the detected hand from the webcam.
	- [HandPose Parts](https://editor.p5js.org/ml5/sketches/DNbSiIYKB): Draw specific hand parts of the detected hand to detect "pinch" gestures
- [FaceMesh](https://docs.ml5js.org/#/reference/facemesh): Detects facial landmarks as coordinates (eyes, mouth, nose, outline of face, etc)
	- [FaceMesh Keypoints](https://editor.p5js.org/ml5/sketches/lCurUW1TT): Draw the keypoints of the detected face from the webcam.
	-   [FaceMesh Parts](https://editor.p5js.org/ml5/sketches/9y9W7eAee): Draw specific face parts of the detected face (mouth)
	- [This Image](https://deckard.openprocessing.org/user398586/visual2096177/hc0589319a18d1b7084a5ed0a9badd00c/image%20(2).png?imageModal=0.6890105623151574) shows the keypoints, numbered – note that it is extremely small

## ml5 + sound example:

- [Pinch-based drum machine](https://craigfahner.github.io/CC2025-cef9489/soundpinch/) - [code](https://github.com/craigfahner/CC2025-cef9489/tree/main/soundpinch)

## More models!

- [Image Classifier](https://docs.ml5js.org/#/reference/image-classifier)
- [Sound Classifier](https://docs.ml5js.org/#/reference/sound-classifier)
- [Sentiment Analysis of Text](https://docs.ml5js.org/#/reference/sentiment)

## p5.sound

To add the p5.sound library, use the following in your index.html file:

    <script src="https://cdn.jsdelivr.net/npm/p5.sound@0.2.0/dist/p5.sound.min.js"></script>
