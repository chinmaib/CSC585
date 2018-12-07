
Experiences Vs Gambles
=====
The repository contains source code for modeling decision-making under risk using fMRI data.  We provide instructions for 
installation of required packages and commands to run the SVM classifier and an LSTM-CRF model that takes fMRI data as input
and predicts the choices made by participants. Please read the [report](https://github.com/chinmaib/CSC585/blob/master/report.pdf) 
for more details on the experiment, data, models, and results.

# Data
Functional Magnetic Resonance Imaging (fMRI) data consists of temporal values of intensities ranging from 0-800
extracted at every [voxel](https://en.wikipedia.org/wiki/Voxel) in the [Hippocampus](https://en.wikipedia.org/wiki/Hippocampus) region of the brain for a period of 20 seconds. The temporal resolution of
functional data is 1 second and spatial resolution is 2.5mm x 2.5mm x 2.9mm.
Every participant makes 10 choices- 5 songs (Experiences) and 5 games (Gambles), wherein each choice they 
were asked to select between a risky (high-variance) choice and a safe (low-variance) choice.

## Testing Data
Test data is located under subjects folder and organized subject-wise. The functioanl data is stored in CSV
folders as CSV files and behavioral data is stores in Behavioral folder as txt files. The folder structure is as below.

...
subjects
  -> Subject2017-03_PD
      --> CSV
          --->Hippocampus
              ----> Subject2017-03_PD_Hippocampus_1.csv
      --> Behavioral
          -- Choice_type.txt
          -- Selections.txt
...

## Running Baseline (SVM)
We make use of (libsvm)[https://www.csie.ntu.edu.tw/~cjlin/libsvm/] library to run the baseline SVM model. 
The (libsvm-3.23)(https://github.com/chinmaib/CSC585/tree/master/libsvm-3.23) folder contains the executable
files svm-train and svm-predict. 


## Running LSTM-CRF
