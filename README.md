# EmoSteer-GNN_pipelines

This is the repository containing our scripts of running F5TTS, EmoSteer and GNNSteer pipelines.
VCTK-Corpus-0.92 (for style cloning) and Ravdess (for extracting emotion) datasets were used throughout these scripts. 
These datasets need to be cloned in your workspace ahead of time. 

F5TTS model was used with pre-trained weights to generate neutral outputs. However, it copies the exact style of the reference audio, leaving little room for emotional manipulation. 

EmoSteer (in review) proposes a training free method to steer the generation towards specific emotions. However, the effects of emotions on the output were still very low. 

We aimed to model a GNN-steering auxillary pipeline, which would learn the adjacencies between the properties of speech from each emotion type, and use them to steer the diffusion vectors strongly.
We also aimed to maintain the interpretibility of the pipeline by training simply the adjacency matrix. This can be improved to attention models in order to capture dependencies better. 
In the initial stages of the project, we are targeting 3 distinct emotions ["happy", "sad", "angry"], which comes from the Ravdess dataset.

