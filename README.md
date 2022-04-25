# DebtVC-for-optimizing-debt-collection

DebtVC is an adaptive voice conversion framework designed to improve debt collection performance. On the basis of fully learning the prosody information of the collectors, it converts the prosody of the bad collectors into the prosody of the good collectors, thereby realizing the improvement of the collection performance of the bad collectors.

## Methodology

Flowchart of DebtVC

- Training phase

![image](https://github.com/DebtVC-lab/DebtVC2021/blob/main/DebtVC_Overview_training.bmp)

- Conversion phase

![image](https://github.com/DebtVC-lab/DebtVC2021/blob/main/DebtVC_Overview_conversion.bmp)

Design motivation of DebtVC forge module

![image](https://github.com/DebtVC-lab/DebtVC2021/blob/main/forge_function_with_arrow.bmp)

If you find this work useful and use it in your research, please consider citing our paper.

## Audio demos

We show some audio demos, and if you want to obtain the large-scale dataset of telephone recordings in the practical scenarios of debt collections, please contact us.

## Dependencies

- Python 3.8
- multiprocessing
- queue
- Numpy
- math
- Scipy
- PyTorch >= v1.2.0
- librosa
- pysptk
- soundfile
- matplotlib
- wavenet_vocoder pip install wavenet_vocoder==0.1.1 for more information, please refer to https://github.com/r9y9/wavenet_vocoder


## To training

The training process of DebtVC consists of two parts, the first is to train the timbre constraint, the prosody constraint and the discriminator, and then further train the reconstruction loss of mel.

Please use the scripts to prepare your own data for training.

- Extract spectrogram and f0(Training phase): python data_loader.py

- Run the training scripts(Training phase): python train.py

- Run the forge scripts(Conversion phase): python forge_demo.py
