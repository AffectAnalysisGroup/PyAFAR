
![pyafar_pipeline](../images/pyafar_pipeline.JPG)

PyAFAR outputs a CSV file with following columns:


- `Frame`: Frame number in the input video
- `Person_ID`: Identifier for an individual in the video, if there are multiple individuals in the input Person_ID can be greater than 1
- `Eye Aspect Ratio`: Ratio of width to height of the eye, this is the mean aspect ratio between the left eye and the right eye
- `Mouth Aspect Ratio`: Ratio of width to height of the mouth


## Tracking

The output CSV file contains predictions for frames where at least individual in the video is detected. Hence the number of unique frames in the CSV could be less than the total number of frames in the input video.


## Head Pose

`Pitch, Yaw, Roll`: Head orientation along Pitch, Yaw and Roll (in degrees or radians?)

## Facial Landmarks

For a given landmark `i` the landmarks in the output CSV are represented using `x_i`, `y_i` and `z_i`. PyAFAR predicts 468 3D (x, y, z) landmarks. 


## Action Unit (AU) Predictions

PyAFAR predicts Action Units using separate prediction models for adults and infants. Note that as not all AU occurrence are predicted for both adults and infants. Predictions available indicated below in `()`. An interactive refresher to AUs can be found [here](https://sites.pitt.edu/~jeffcohn/FACSmodule.html).

The AU detector module of PyAFAR can predict occurrence and intensity of the following action units. 

### Occurrence

```
AU 1 (adult, infant): Inner Brow Raise
AU 2 (adult, infant): Outer Brow Raise
AU 3 (infant only): 
AU 4: Brow Lowerer
AU 6 (adult, infant): Cheek Raise
AU 7 (adult only): Lids Tight
AU 9 (infant only): Nose wrinkle
AU 10 (adult only): Upper Lip Raiser
AU 12 (adult, infant): Lip Corner Puller
AU 14 (adult only): Dimpler
AU 15 (adult only): Lip Corner Depressor
AU 17 (adult only): Chin Raiser
AU 20 (infant only): Lip Stretch
AU 23 (adult only): Lip Tightener
AU 24 (adult only): Lip Presser
AU 28 (infant only): Lip Suck
```

where `Occ_au_i` column in the CSV is the likelihood of `AU i` expressed by `Person_ID` in the frame. 


### Intensity

```
AU 6 (adult only)
AU 10 (adult only)
AU 12 (adult only)
AU 14 (adult only)
AU 17 (adult only)
```

where `Int_au_i` column in the CSV is the intensity of `AU i` expressed by `Person_ID` in the frame. Intensity predictions lie in [0, 5] range.


## Visualization

PyAFAR can predict various face based affect related features as demonstrated below

![demo_gif](../images/pyafar_demo.gif)