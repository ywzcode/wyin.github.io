Traditional problems:
1. requiring large amounts of labelled data. For learning low-level correspondence, such as optical flow, synthetic computer graphics data.
2.  learning higher-level semantic correspondence rely on human annotation

3. Tracking requires a model of visual invariance.

Key Idea:
We can obtain unlimited supervision for correspondence by tracking forward and backward and using inconsistency between the start and end points as the loss function.
As the feature for identifying correspondences across frames improves, the ability of tracking improves. 

Without additional constraints, learning can take shortcuts, making correspondences cycle-consistent but wrong.

a track that never moves is inherently cycle-consistent.

cycle-consistency may not be achievable due to sudden changes in object pose or occlusions; skip-cycles can allow for cycle- consistency by skipping frames.


Temporal structure serves as a useful signal for learning because the visual world is continuous and smoothly-varying

Spatiotemporal stability is thought to play a crucial role in the development of invariant representations in biological vision

Tow learning problems (learning representation and tracking) are complementary.

Classic approaches to tracking treat it as a matching problem, where the goal is to find a given object/patch in the next frame. key challenge is to track reliably over extended time periods.

 researchers largely turned to “track- ing as repeated recognition”, where trained object detectors are applied to each frame independently.
 
 descriptor that matches region hierarchies and provides dense and sub-pixel level estimation of flow.
 
 finding mid-level correspondences between regions across different scenes.
 
 Advantage of this model: they address the problems of learning representations of correspondence without human annotations.
 
 The goal is to learn a feature space $\varphi$ by tracking a patch pt extracted from image $I_{t}$ backwards and then forwards in time, while minimizing the cycle-consistency loss $l_{\theta}$ (yellow arrow).
 
 
 
 



