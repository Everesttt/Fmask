# Fmask
The software called Fmask (Function of mask) is used for automated clouds, cloud shadows, and snow masking for Landsats 4-7, Landsat 8, and Sentinel 2 images.

If you have any questions, please contact Zhe Zhu (zhe.zhu@ttu.edu) at Department of Geosciences, Texas Tech University.

**IMPORTANT:** Fmask 4.0 softwares (including standalones with GUI and without GUI) on Windows (~1G) is ready to use now! It can be downloaded at this [link] (https://drive.google.com/drive/folders/1SXBnEBDJ1Kbv7IQ9qIgqloYHZfdP6O1O). This version has substantial better cloud, cloud shadow, and snow detection results for Sentinel 2 and better results (compared to the 3.3 version that is currently being used by USGS as the Collection 1 QA Band) for Landsats 4-8 . This one software can be used for **Landsats 4-8 Collection 1 Level 1 product** and **Sentinel 2 Level-1C product** at the same time.

**IMPORTANT:** Majority of the current Collection 1 Landsats 4-8 QA Band provided by USGS are derived form 3.3 Version of Fmask algorithm based on default parameters (cloud probability is 22.5% and buffer pixel size is 3). For example, (1) The Cloud (bit 4) is based on Fmask cloud mask (0 is not cloud and 1 is cloud in Fmask); (2) The Cloud Confidence (bits 5-6) is based on Fmask cloud probability in which >22.5% is high (11), >12.5% is medium (10), and <12.5% is low (01) with 00 kept for future use; (3) Snow/ice Confidence (bits 9-10) and Cloud Shadow Confidence (bits 7-8) has only low confidence (01) and high confidence (11) which correspond to no and yes respectively in snow/ice and cloud shadow mask provided by Fmask.

# 4.0 Version

1) Published Fmask 4.0 verion. (Shi Qiu, Zhe Zhu, and Binbin He 04/26/2018)

2) Adjusted the erosion value that will result in many omission errors for small clouds.  (Shi Qiu and Zhe Zhu 04/05/2018)

3) Restricted the height of the clouds located in the scene boundary into the predicted cloud height derived from its neighboring clouds.  (Shi Qiu 04/05/2018)

4) Removed the overlap between the predicted cloud shadow and the potential cloud shadow layer for cloud shadow detection. (Shi Qiu and Zhe Zhu 03/29/2018)

5) Fixed the bug that the reading blue band using GRIDobj may lead to Nan value for Landsat images. (Shi Qiu 03/26/2018)

6) Improved the computational efficiency specially for cloud shadow matching procedure.  (Zhe Zhu and Shi Qiu 03/24/2018)

7) Published Fmask 4.0 beta version. (Shi Qiu, Zhe Zhu, and Binbin He 03/22/2018)
