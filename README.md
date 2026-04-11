# Emotion Steering for Text-to-Speech via Graph-Based Feature Manipulation

This is the repository containing our scripts of running F5TTS, EmoSteer and GNNSteer pipelines as a part of our Deep Learning Semester Project.
We aimed to model a GNN-steering auxillary pipeline, which would learn the adjacencies between the properties of speech from each emotion type, and use them to steer the diffusion vectors strongly.
We also aimed to maintain the interpretibility of the pipeline by training simply the adjacency matrix. This can be improved to attention models in order to capture dependencies better. 
In the initial stages of the project, we are targeting 3 distinct emotions ["happy", "sad", "angry"], which comes from the Ravdess dataset.

### Description of Execution
All the files (.py files and .sh file) in the main branch are students' works, only taking inspiration from F5TTS inference files and the EmoSteer paper.
#### Dataset
VCTK-Corpus-0.92 (for style cloning) and Ravdess (for extracting emotion) datasets were used throughout these scripts. 
These datasets need to be cloned in your workspace ahead of time. 

#### Models
F5TTS model was used with pre-trained weights to generate neutral outputs. However, it copies the exact style of the reference audio, leaving little room for emotional manipulation. 

EmoSteer (in review) proposes a training free method to steer the generation towards specific emotions. However, the effects of emotions on the output were still very low. 

The GNNSteer pipeline leaves a few things for improvement. Its outputs show results only in evaluation metrics but sounds extremely similar to human ears.


## Acknowledgements

This project builds upon the official open-source implementation of **F5-TTS** by Chen et al.
The original repository provides the base model architecture, training framework, and inference pipeline.

Original repository:
https://github.com/SWivid/F5-TTS

All additional components in this repository—including GNNSteer, EmoSteer integration were developed by the authors of this project.
