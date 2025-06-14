# AI-Assisted Colonoscopy Navigation — Predicting Insertion Direction
### Introduction/Project Aim


Colonoscopy is a vital tool in the early detection and diagnosis of colorectal diseases. However, navigating the colonoscope through the complex, curved, and often poorly visualized intestinal tract remains a major challenge. During insertion, physicians often face ambiguous views, sharp bends, and limited visibility, increasing procedure time, patient discomfort, and the risk of complications. To address these challenges, we propose an AI-assisted navigation system for colonoscopy, aimed at predicting the optimal insertion direction based on real-time endoscopic imagery.This system leverages deep learning and image processing techniques to analyze colonoscopic video frames and assist clinicians in guiding the scope more efficiently and safely. 

### Previous Work
Despite the anatomical complexity of the gastrointestinal (GI) tract, its relatively large lumen and good visibility have encouraged extensive global research into autonomous visual navigation methods for endoscopy. Prior work mainly falls into two categories:
(1) Dark region and optical flow-based approaches, which identify the darkest or deepest regions in an image as a proxy for the lumen center [1–9].
These methods are simple to implement, and many studies have explored segmenting dark areas or estimating 3D depth using shadows or light gradients. However, they share a fundamental limitation: the assumption that the darkest point always represents the optimal forward direction. In reality, this assumption is easily disrupted by lighting conditions, camera focus, and tissue geometry. Most of these methods ignore endoscope size and surrounding anatomy, which often leads to suboptimal navigation—especially in curved or complex sections of the colon. While the darkest region may align well in straight segments like the descending colon, it fails in tortuous or occluded areas where proper alignment requires more anatomical awareness.
(2) Lumen centralization methods based on anatomical features, such as haustral folds or lumen contours.
These methods often offer more reliable direction cues, as visible structures like folds are typically closer to the endoscope and better reflect the actual lumen path. However, such features are not always visible—especially in occluded views or sharp turns where the scope directly faces the colon wall.
Overall, a robust navigation algorithm must adapt to highly variable anatomical environments and be resilient across patients, accommodating both visual clarity and structural occlusions during insertion.

### Our Method
To address the complexity and variability of the gastrointestinal environment, we propose a navigation method that predicts the insertion direction by combining lumen image classification with both dark-region analysis and haustral fold-based tracking. Our system consists of three key components: a lumen image classifier, a dark-region-based lumen center estimator, and a fold-based lumen tracking algorithm. The process begins by classifying each frame into two categories based on visual features: images with clear haustral folds are routed to the fold-based algorithm, while those showing ambiguous or poorly structured regions (e.g., sharp turns or occlusions) are processed using the dark-region method. This adaptive framework allows the system to select the most suitable strategy based on the current visual context, improving the accuracy and robustness of lumen center detection and forward direction prediction during colonoscope insertion.





#### Reference Paper
1.https://arxiv.org/pdf/1807.10165


### DataSets 
