# Prediction of Large Solar Flares Based on SHARP and HED Magnetic Field Parameters

The repository includes HED and SHARP Datasets, along with descriptions of the data processing procedures, and the experimental code utilized in our study.

The file named "The data for Prediction of Large Solar Flares Based on SHARP and HED Magnetic Field Parameters" contains the raw data of HED and SHARP Datasets. Each dataset consists of 286 ARs, specifically, each dataset includes 189 C-class flaring ARs, 86 M-class flaring ARs, and 11 X-class flaring ARs. The column name "AR" represents the NOAA AR numbers, the column name "time" represents the time at which the AR samples were acquired, and the column name "level" represents the flare class of the AR. Moreover, in the HED dataset, the column name "energy" represents the "E_{free}", "shear_mean" represents the "\Psi", "uj_mean" represents the "J_{Z}", "uhc_mean" represents the "H_{C}", "GBH_MEAN" represents the "B_{h}", and "ALP_MEAN" represents the "\alpha". In the SHARP dataset, the column names of the other columns correspond to the names of various parameters.

The files named "SHARP_CV" and "HED_CV" represent the ten cross-validation sets that have been normalized and divided using an AR-based cross-validation method.
The data processing procedures are as follows. Since the SHARP and HED parameters have distinct scales and units, they are individually normalized using mean-standard deviation. Subsequently, we set the labels for C-class flaring ARs to negative class(0), and the labels for M/X-class flaring ARs to positive class(1). We employ an AR-based cross-validation (CV) method to partition the SHARP and HED datasets with the distribution of the training, validation, and testing sets at a ratio of 60%, 20%, and 20%, respectively. This process is repeated ten times, resulting in ten cross-validation sets in both SHARP datasets (SHARP_CV) and HED datasets (HED_CV), respectively. The column named "level" in the SHARP_CV data and the column named "key" in the HED_CV data represent the labels for the flare classes of the ARs.

We design five solar flare prediction models leveraging five currently popular deep learning algorithms: Transformer, BiLSTM-Attention, BiLSTM, LSTM-Attention, and LSTM. Moreover we use the NN model as the baseline model to compare with other deep learning model. The solar flare prediction model used in this paper can be accessed via https://drive.google.com/drive/folders/1n6fXcQdCBogKt6L0aaPFagraFcXmX0fw?usp=drive_link.

![SHARP parameters](https://github.com/user-attachments/assets/0a38f2c7-862f-417d-8f02-318e0afa80f4)

![HED parameters](https://github.com/user-attachments/assets/b941cd5c-5e57-4587-8d7a-46b5f16fb578)
