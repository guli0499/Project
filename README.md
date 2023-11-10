# Project
Preparing the dataset
Resampling to 44100Hz Mono
python resample.py
Automatic partitioning of training set, validation set, and automatic generation of profiles
python preprocess_flist_config.py --speech_encoder vec768l12
Generate hubert with f0
python preprocess_hubert_f0.py --f0_predictor dio
Main Model Training
python train.py -c configs/config.json -m 44k
Launching the Web GUI
python webUI.py
