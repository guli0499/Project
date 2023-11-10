# Project
dataset, pretrain model and else:https://drive.google.com/drive/folders/1rGjlqPWn28hiGniy4DEGdOrPOWXIdqGB?usp=drive_link
Preparing the dataset  
Resampling to 44100Hz Mono  
```
python resample.py
```
Automatic partitioning of training set, validation set, and automatic generation of profiles  
```
python preprocess_flist_config.py --speech_encoder vec768l12
```
Generate hubert with f0  
```
python preprocess_hubert_f0.py --f0_predictor dio
```
Main Model Training  
```
python train.py -c configs/config.json -m 44k
```
Launching the Web GUI  
```
python webUI.py
```
The training was eventually completed, but the results were unsatisfactory and the clutter was heavy. It could be a parameter setting problem.
