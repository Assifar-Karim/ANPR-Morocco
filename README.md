# ANPR-Morocco
-> Read this in [French](https://github.com/Assifar-Karim/ANPR-Morocco/blob/main/FR-README.md) <br/>
ANPR-Morocco is an automatic number plate recognition system for moroccan license plates. This repository contains three versions of the system that have been updated in an incremental way to get better recognition results. <br/>
The first version of the system relies on classical OCR techniques to extract the license plate from the used image and uses Tesseract OCR to read the characters from the extracted plate, to enhance the quality of the number plate extraction the classical OCR techniques were substitued with the YoloV4 algorithm that was trained using the Google Open Images Dataset. Finally, using Tesseract OCR or EasyOCR to read the license plates' characters proved to be rather innefficient so as a solution to this issue, the third version relies 100% on the YoloV4 algorithm that was trained on a specific dataset taken from the Mohammed VI Polytechnic University MSDA website. 
#### Mean average precision table for the two YoloV4 Models:

| Model | YoloV4 for plate detection | YoloV4 for character detection |
|-------|----------------------------|--------------------------------|
| MaP   | 90.17%                     | 81.45%                         |

#### How to use the project
To use the project, download the weights and config files from the Models Data directory then download the `Licence_ Plate_Recognizer_V3.0` notebook and open it either on google colaboratory or on a local jupyter notebook instance.
 If the jupyter notebook instance is local then the user must install YoloV4 and darknet beforehand. To do that, please refer to  https://github.com/AlexeyAB/darknet.<br/>
 If the user decides to use google colaboratory, then the weights and config files can be stored on a google drive to make it easier to use with the notebook. 

#### References
 - Link to the dataset used in the V3 training : https://msda.um6p.ma/msda_datasets <br/>
 - Link to the paper the V3 character recognition is based on : https://arxiv.org/pdf/2104.08244.pdf
