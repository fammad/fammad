## Hi, I'm Fuad

I spent four years in Ritual Theater lab in Baku by putting technology on stage. I developed XR experiences where 600 people walked through. A robot bear that talks back to children. Projection, motion capture, a lot of gaffer tape. Somewhere in there I noticed that the interesting problems were all the same problem, which is a camera trying to work out what a person is paying attention to.

So now I'm at KTH in Stockholm doing a master's in Interactive Media Technology, and I work on eye tracking and computer vision. I have studied B.Eng. Mechatronics and Robotics by training. I like building the whole loop, from the camera to the model to the thing that moves or lights up on the desk.

### Research focus

**Gaze estimation and eye tracking.** Appearance-based gaze estimation from monocular RGB, blink and eye-state detection from facial landmarks, and the evaluation protocols that make those numbers mean something (person-independent splits, angular error, cross-condition validation).

**Where it's going.** Assistive technology, where gaze is an input channel for people who can't use a keyboard or a touchscreen, and attention monitoring, where blink rate and gaze direction are signals of fatigue and distraction.

**How I work.** Build the full sensor-to-actuator loop, measure it under the ugly conditions first, and write the failure cases into the README next to the headline number.

### Projects

#### Gaze and eye tracking

**[GazeMap](https://github.com/fammad/GazeMap)** · appearance-based gaze estimation · PyTorch, MPIIGaze
A compact CNN regresses gaze pitch and yaw from a 36×60 normalized eye crop, evaluated by mean angular error on the 3D gaze vector. The first number I got beat the published baselines, which is how I learned that MPIIGaze frames come from continuous recordings and a random split leaks near-duplicate frames into validation. The repo now uses leave-one-person-out cross-validation across all 15 subjects and keeps the leaky 4.01° in the README as a warning label. Next is head pose as a second input.

**[Lumen](https://github.com/fammad/Lumen_blink_detection)** · blink detection, hardware in the loop · OpenCV, MediaPipe, ESP32-S3
Blink rate drops during sustained screen work. Lumen detects blinks from MediaPipe Face Mesh landmarks using the eye aspect ratio, tracks a rolling personal baseline seeded with a literature prior, scores strain, and drives a silicone dome on the desk from white to amber to red over serial. No notifications, no frames written to disk. F1 0.92 under ±45° head turns at 1 m, validated against manual counts in six lighting and distance conditions, with the failure envelope documented (2 m under lamp light, tinted glasses, head turns past 30°).

#### Human-robot interaction

**[Qonur](https://github.com/fammad/Qonur_Robotic_Bear)** · social robot for children · Python, Gemini API, ESP32, Fusion 360
A conversational animatronic bear that listens and answers in Azerbaijani, built for anti-bullying theatre with children. Speech in, LLM reply, TTS out, with mouth positions streamed to an ESP32 driving ten servos over PCA9685 as JSON over USB serial. Full autonomy was the plan until we measured a multi-second cloud round trip against a six-year-old's patience, so the dialogue is AI and the choreography is a human operator with a phone. I led mechanics, 3D modelling and the portable design. Deployed in a children's shelter and a rural village, print files included, SDC-funded.

#### Machine learning

**[EmotionRadar](https://github.com/fammad/EmotionRadar)** · multi-label text classification · scikit-learn, NLTK
Seven Ekman emotions from 58k GoEmotions Reddit comments. One-vs-rest logistic regression with class-balanced weights over 1–2 gram TF-IDF doubles the Naive Bayes baseline's macro-F1 (0.25 to 0.51), and every prediction traces back to the words that drove it. The result I'm most attached to is negative. Emotions don't cluster in TF-IDF/LSA space, shown three ways (DBSCAN eps sweep, K-Means silhouette and ARI, t-SNE), and we wrote that up instead of quietly picking a model that hid it. Reproducible top to bottom in one Colab notebook.

### Toolbox

| | |
|---|---|
| Computer vision | OpenCV, MediaPipe (Face Mesh, landmarks), eye aspect ratio, image normalization, dataset inspection and visualization |
| Machine learning | PyTorch (CNN regression, custom Dataset/DataLoader), scikit-learn (linear models, clustering, TF-IDF, LSA), NumPy, pandas |
| Evaluation | leave-one-person-out and subject-aware splits, leakage checks, angular error, macro/micro-F1, ROC-AUC, per-condition validation tables, seeded and reproducible runs |
| Embedded and hardware | ESP32 / ESP32-S3, Arduino, PCA9685 servo control, NeoPixel, USB serial protocols, Fusion 360, FDM 3D printing |
| XR and media | Unity (C#), MOVE AI body capture, Blender, Figma, After Effects |
| Languages | Python, C++ for firmware, C# for Unity |

### Now

Person-independent gaze error on MPIIGaze, then head pose as a second input. Two computer vision courses this autumn at KTH (Analysis and Search of Visual Data, Image Analysis and Computer Vision). Looking for a master's thesis in eye tracking or computer vision for 2027.

### Elsewhere

[fammad.com](https://fammad.com) · [LinkedIn](https://www.linkedin.com/in/fammad/) · hej@fammad.com

