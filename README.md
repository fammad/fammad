## Hi, I'm Fuad

I build eye tracking systems end to end: the camera, the pupil or gaze model, the calibration, and the honest number at the end. Right now that means a webcam gaze estimator, an infrared tracker I built into a Meta Quest 3, and a blink-fatigue detector that drives a light on the desk.

Before KTH I spent four years at Ritual Theater lab in Baku putting technology on stage: XR experiences 600 people walked through, a robot bear that talks back to children, projection and motion capture. The interesting problem kept being the same one, a camera trying to work out what a person is paying attention to. So I came to KTH in Stockholm for a master's in Interactive Media Technology, after a B.Eng. in Mechatronics and Robotics.

**Looking for a master's thesis in 2027** in eye tracking, driver and occupant monitoring, gaze in XR, or gaze-based assistive technology.

### What I work on

**Gaze from cameras that were not built for it.** Appearance-based gaze estimation from a laptop webcam, and pupil tracking from a cheap infrared camera inside a VR headset. Both evaluated on data the model never saw.

**What gaze can and cannot tell you.** Which metrics survive real accuracy: dwell on large objects yes, small tools no; head direction is not gaze; a calibration fit is not accuracy. I write the failure cases next to the headline number.

**Where it goes.** Attention and fatigue in vehicles, training and skills assessment in XR, and gaze as an input channel for people who cannot use their hands.

### Projects

#### Eye tracking

**[gaze-XR-training](https://github.com/fammad/gaze-XR-training)** · eye tracking in VR · Unity, C#, Python, OpenCV, Quest 3
The Quest 3 has no eye tracker, so I glued an infrared camera under the lens. A pupil detector on the Mac follows the pupil outline even when the LEDs make it half bright and half dark, and streams gaze to a Unity toolkit that does 9-dot calibration, fixations, scanpath, heatmaps, areas of interest and synced session logging. The finding I care about: calibration fits to 0.8°, but an independent grid says about 5°, growing as the headset slips. That decides which training metrics you can trust, and the README turns it into a blueprint. Works with any gaze source, so the Unity side runs on headsets with built-in tracking too.

**[GazeMap](https://github.com/fammad/GazeMap)** · webcam gaze estimation · PyTorch, MediaPipe, MPIIGaze
A small CNN trained from scratch on 427k eye images, tested leave-one-person-out on all 15 MPIIGaze subjects: 4.97° with both eyes fused, 3.98° after a short calibration from another day, 1.55° (1.9 cm on screen) in the live demo. The failure analysis maps head rotation, occlusion, noise, blur and low light. My first number beat the published baselines, which is how I learned that random splits leak near-duplicate frames; the repo keeps that lesson in. Training three times longer did nothing for unseen people.

**[Lumen](https://github.com/fammad/Lumen_blink_detection)** · blink and fatigue detection · OpenCV, MediaPipe, ESP32-S3
Blink rate drops during sustained screen work. Lumen detects blinks from Face Mesh landmarks with the eye aspect ratio, tracks a rolling personal baseline, scores strain and drives a silicone dome on the desk from white to amber to red. No notifications, no frames saved. F1 0.92 with head turns up to ±45° at 1 m, validated in six lighting and distance conditions, failure envelope documented (2 m under lamp light, tinted glasses, head turns past 30°).

#### Human-robot interaction

**[Qonur](https://github.com/fammad/Qonur_Robotic_Bear)** · social robot for children · Python, Gemini API, ESP32, Fusion 360
A conversational animatronic bear that answers in Azerbaijani, built for anti-bullying theatre. Speech in, LLM reply, TTS out, mouth positions streamed to ten servos. Full autonomy was the plan until a multi-second cloud round trip met a six-year-old's patience, so the dialogue is AI and the choreography is a human operator. Deployed in a children's shelter and a rural village, print files included.

#### Computer vision and machine learning

**[vocab-tree-image-retrieval](https://github.com/fammad/vocab-tree-image-retrieval-EQ2425)** · image retrieval · SIFT, hierarchical k-means, TF-IDF, OpenCV
**[EmotionRadar](https://github.com/fammad/EmotionRadar)** · multi-label text classification · scikit-learn. Macro-F1 from 0.25 to 0.51, plus a negative result written up honestly: emotions do not cluster in TF-IDF space.

### Toolbox

| | |
|---|---|
| Eye tracking | pupil detection and ellipse fitting (RANSAC), appearance-based gaze estimation, calibration (polynomial, affine), accuracy and precision grids, I-VT fixation detection, AOI analysis, blink detection (EAR) |
| Computer vision and ML | OpenCV, MediaPipe, PyTorch, scikit-learn, NumPy, pandas, Matplotlib |
| Evaluation | leave-one-person-out splits, leakage checks, angular error, per-condition failure analysis, reproducible seeded runs |
| XR | Unity 6 (C#, URP, OpenXR, XR Interaction Toolkit), Meta Quest, session recording and sync |
| Hardware | IR camera modules, ESP32 / ESP32-S3, Arduino, servo control, USB serial, Fusion 360, 3D printing |
| Languages | Python, C#, C++ for firmware |

### Now

Two computer vision courses at KTH this autumn (Analysis and Search of Visual Data, Image Analysis and Computer Vision). Next on the headset tracker: slip correction with corneal glints and gaze from commercial headsets through OpenXR.

### Elsewhere

[fammad.com](https://fammad.com) · [LinkedIn](https://www.linkedin.com/in/fammad/) · hej@fammad.com
