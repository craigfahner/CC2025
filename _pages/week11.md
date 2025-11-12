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

Note that facemesh has hundreds of keypoints, so it can be difficult to identify which point is related to which part of the face. The model provides subsets (or "annotations") of facial features, which only contain the coordinates for their respective features: 

    • silhouette
    • lipsUpperOuter
    • lipsLowerOuter
    • lipsUpperInner
    • lipsLowerInner
    • rightEyeUpper0
    • rightEyeLower0
    • rightEyeUpper1
    • rightEyeLower1
    • rightEyeUpper2
    • rightEyeLower2
    • rightEyeLower3
    • rightEyebrowUpper
    • rightEyebrowLower
    • leftEyeUpper0
    • leftEyeLower0
    • leftEyeUpper1
    • leftEyeLower1
    • leftEyeUpper2
    • leftEyeLower2
    • leftEyeLower3
    • leftEyebrowUpper
    • leftEyebrowLower
    • midwayBetweenEyes
    • noseTip
    • noseBottom
    • noseRightCorner
    • noseLeftCorner
    • rightCheek
    • leftCheek

In the following example, I'm just extracting the silhouette group, drawing it to the screen as a shape with vertices. I've created a new function called drawFace to do this:

    function drawFace() {
    	if (predictions.length > 0) {
    		let keypoints = predictions[0].annotations.silhouette;
    		beginShape();
    		for (let i = 0; i < keypoints.length; i++) {
    			const [x, y] = keypoints[i];
    			fill(255,50);
    			vertex(x, y);
    		}
    		endShape();
    	}
    }
