## Hi, I'm Fuad

I build systems that understand people through sensors and respond to them: computer vision and machine learning on one end, XR, robots and embedded hardware on the other. I take them from the raw signal to a working prototype people can use, and I measure where they fail before I report what they do.

MSc Interactive Media Technology at KTH, Stockholm · B.Eng. Mechatronics and Robotics · **looking for a 2027 master's thesis** in computer vision, human-centred AI, XR or perception for vehicles and robots.

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white) ![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white) ![MediaPipe](https://img.shields.io/badge/MediaPipe-0097A7?style=flat-square&logo=google&logoColor=white) ![Unity](https://img.shields.io/badge/Unity-000000?style=flat-square&logo=unity&logoColor=white) ![C#](https://img.shields.io/badge/C%23-512BD4?style=flat-square&logo=dotnet&logoColor=white) ![ESP32](https://img.shields.io/badge/ESP32-E7352C?style=flat-square&logo=espressif&logoColor=white)

### Projects

<table>
<tr>
<td width="50%" valign="top">
<a href="https://github.com/fammad/gaze-XR-training"><img src="https://raw.githubusercontent.com/fammad/gaze-XR-training/main/media/header.gif" width="100%" alt="Fixations, scanpath and heatmap in a VR workbench, with the IR eye camera in the corner"></a>
<br><sub>EYE TRACKING · XR</sub>
<br><b><a href="https://github.com/fammad/gaze-XR-training">gaze-XR-training</a></b>
<br>An infrared camera glued under a Quest 3 lens, a pupil tracker and a Unity gaze toolkit. Calibration fit <b>0.8°</b>, independent grid <b>about 5°</b>, and a blueprint of which training metrics that accuracy supports.
<br><sub>Unity · C# · Python · OpenCV · Quest 3</sub>
</td>
<td width="50%" valign="top">
<a href="https://github.com/fammad/GazeMap"><img src="https://raw.githubusercontent.com/fammad/GazeMap/main/assets/demo_pedestrians.gif" width="100%" alt="Gaze trail over a street scene next to the webcam image"></a>
<br><sub>EYE TRACKING · DEEP LEARNING</sub>
<br><b><a href="https://github.com/fammad/GazeMap">GazeMap</a></b>
<br>A CNN trained from scratch on 427k eye images, tested on people it never saw: <b>3.98°</b> after calibration, <b>1.55°</b> in the live demo, with a full failure analysis.
<br><sub>PyTorch · MediaPipe · OpenCV · MPIIGaze</sub>
</td>
</tr>
<tr>
<td width="50%" valign="top">
<a href="https://github.com/fammad/vehicle-trajectory-generation"><img src="https://raw.githubusercontent.com/fammad/vehicle-trajectory-generation/main/docs/flow_ABCD.gif" width="100%" alt="Twenty generated futures for one left-turning car under four constraint strategies"></a>
<br><sub>AUTOMOTIVE · GENERATIVE MODELS · TEAM</sub>
<br><b><a href="https://github.com/fammad/vehicle-trajectory-generation">Vehicle trajectory generation</a></b>
<br>Flow Matching on drone recordings of an Aachen intersection (inD). Without road rules <b>28 %</b> of generated futures leave the road; soft guidance fixes that at no cost in smoothness, while hard projection multiplies jerk up to <b>5×</b>.
<br><sub>PyTorch · Flow Matching · inD dataset</sub>
</td>
<td width="50%" valign="top">
<a href="https://github.com/fammad/Lumen_blink_detection"><img src="https://raw.githubusercontent.com/fammad/Lumen_blink_detection/main/assets/lumen.jpeg" width="100%" alt="Lumen silicone light dome in different states"></a>
<br><sub>ATTENTION · EMBEDDED · NORDICHI 2026 DEMO SUBMISSION</sub>
<br><b><a href="https://github.com/fammad/Lumen_blink_detection">Lumen</a></b>
<br>Blink rate from a webcam drives a silicone light on the desk from white to amber to red. <b>F1 0.92</b> with head turns up to ±45°. No frames saved, no cloud, failure envelope documented.
<br><sub>MediaPipe · OpenCV · ESP32-S3 · C++</sub>
</td>
</tr>
<tr>
<td width="50%" valign="top">
<a href="https://github.com/fammad/Qonur_Robotic_Bear"><img src="https://raw.githubusercontent.com/fammad/Qonur_Robotic_Bear/main/assets/Image_Qonur_front-back.png" width="100%" alt="Qonur robot bear, front and back"></a>
<br><sub>HUMAN-ROBOT INTERACTION · SDC-FUNDED</sub>
<br><b><a href="https://github.com/fammad/Qonur_Robotic_Bear">Qonur</a></b>
<br>A talking animatronic bear for anti-bullying theatre: AI conversation, human-operated choreography, ten servos. Deployed in a children's shelter and a rural village. <a href="https://www.youtube.com/watch?v=doGUTJyK8F4">Watch it perform</a>.
<br><sub>Python · Gemini API · ESP32 · Fusion 360</sub>
</td>
<td width="50%" valign="top">
<a href="https://github.com/fammad/tbana-perceived-safety"><img src="https://raw.githubusercontent.com/fammad/tbana-perceived-safety/main/assets/cover_4x3.jpg" width="100%" alt="Child and caregiver at the edge of a VR subway platform with glass doors"></a>
<br><sub>XR USER STUDY · HUMAN PERCEPTION · TEAM</sub>
<br><b><a href="https://github.com/fammad/tbana-perceived-safety">Perceived safety on a T-bana platform</a></b>
<br>A within-subject VR study on a Quest 2: 16 randomised scenes, 7 participants, four factors (child or adult, crowd, caregiver, glass doors). Doors raised felt safety in every condition; a child alone at a crowded open edge scored lowest, about <b>1.9 of 5</b>.
<br><sub>Unity · Quest 2 · Likert survey · KTH DM2350</sub>
</td>
</tr>
</table>

### How I work

I build the whole loop, from the sensor to the model to the thing that moves or lights up. I measure under the ugly conditions first: unseen people, turned heads, a headset that slips. And I write the failure cases next to the headline number, because a calibration fit is not accuracy and a random split is not a test.

Before KTH I spent four years at Ritual Theater lab in Baku putting technology on stage: XR experiences 600 people walked through, a robot bear that talks back to children, projection and motion capture. The interesting problem kept being the same one, a camera trying to work out what a person is paying attention to.

<details>
<summary><b>Toolbox</b></summary>
<br>

| | |
|---|---|
| Eye tracking | pupil detection and ellipse fitting (RANSAC), appearance-based gaze estimation, polynomial and affine calibration, accuracy and precision grids, I-VT fixations, AOI analysis, blink detection (EAR) |
| Computer vision and ML | OpenCV, MediaPipe, PyTorch (CNNs, Flow Matching), scikit-learn, NumPy, pandas, Matplotlib |
| Evaluation | leave-one-person-out splits, leakage checks, angular error, per-condition failure analysis, seeded reproducible runs |
| XR | Unity 6 (C#, URP, OpenXR, XR Interaction Toolkit), Meta Quest, synced session recording |
| Hardware | IR camera modules, ESP32 / ESP32-S3, Arduino, servo control, USB serial, Fusion 360, 3D printing |
| Languages | Python, C#, C++ for firmware |

</details>

### Now

Two computer vision courses at KTH this autumn, including a vocabulary-tree image retrieval system built from scratch (SIFT, hierarchical k-means, TF-IDF). Next on the headset tracker: slip correction with corneal glints and gaze from commercial headsets through OpenXR.

[fammad.com](https://fammad.com) · [LinkedIn](https://www.linkedin.com/in/fammad/) · hej@fammad.com
