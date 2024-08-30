# Prediction of Large Solar Flares Based on SHARP and HED Magnetic Field Parameters

The dataset used in this paper for SHARP parameters and HED parameters is sourced from "The data for Prediction of Large Solar Flares Based on SHARP and HED Magnetic Field Parameters."

Since the SHARP and HED parameters have distinct scales and units, these parameters were individually normalized using StandardScaler.

Then the SHARP and HED datasets employed an AR-based cross-validation method to partition, with the distribution of the training, validation, and testing sets at a ratio of 60%, 20%, and 20%, respectively. This process is repeated ten times, resulting in ten cross-validation sets in both SHARP_CV and HED_CV.

The solar flare prediction model used in this article can be accessed via https://drive.google.com/drive/folders/1n6fXcQdCBogKt6L0aaPFagraFcXmX0fw?usp=drive_link

In the HED parameters dataset, the column name "energy" represents the "E_{free}","shear_mean" represents the "\Psi","uj_mean" represents the "J_{Z}","uhc_mean" represents the "H_{C}","GBH_MEAN" represents the "B_{h}","ALP_MEAN" represents the "\alpha".

The calculation methods of SHARP and HED parameters are shown in the following figure.

![SHARP parameters](https://github.com/user-attachments/assets/0a38f2c7-862f-417d-8f02-318e0afa80f4)

![HED parameters](https://github.com/user-attachments/assets/b941cd5c-5e57-4587-8d7a-46b5f16fb578)
