# Digitization of Handwritten Answer Script

## Problem Statement Overview
The task involves developing a deep learning model to facilitate the digitization of handwritten answer scripts. Traditional methods of grading involve manual assessment by teachers, which can be time-consuming and prone to errors. Automating this process offers advantages such as faster grading, consistency, and scalability.

## Directory Structure
| File/Folder                     | Description                                                |
|-----------------------------------|------------------------------------------------------------|
| `handwritten-answer-scripts-digitization.ipynb` | Jupyter Notebook containing the main project code.    |
| line-segmentation                 | Directory containing notebook related to line segmentation. |
| passage-identification            | Directory containing notebook related to passage identification. |
| spelling-correction               | Directory containing notebook related to spelling correction. |
| word-recognition                  | Directory containing notebook related to word recognition. |
| word-segmentation                 | Directory containing notebook related to word segmentation. |

## Instructions
- To view the outputs, import the notebook `handwritten-answer-scripts-digitization.ipynb` in Kaggle (with GPUs).
- To view the notebook in Google Colab, click [here](https://colab.research.google.com/drive/1fcPTvCasFQZnPm79pRcItQzTNUgfCwo8).

## Dataset
We utilize the IAM Handwriting Database, which contains 13,353 images of handwritten lines of text from 657 writers. The dataset is labeled at the sentence, line, and word levels, making it suitable for training our models.

## Solution Strategy
1. **Passage Identification:** Predicting the location of handwritten passages using a fine-tuned ResNet34 model.
2. **Line Segmentation:** Segmenting passages into individual lines with a U-Net architecture.
3. **Word Segmentation:** Segmenting lines into words using a Faster RCNN ResNet50 FPN model.
4. **Word Recognition:** Recognizing text from word images with a (CNN + RNN) based model.

## Innovations
- Employing computationally efficient architectures.
- Utilizing U-Net for line segmentation.
- Generating datasets using computer vision techniques.

## Challenges
- Addressing issues with the CTC loss metric for line text recognition.
- Implementing a spelling checker for recognized text.

## Results
The model achieved a Character Error Rate (CER) of 0.3449 on a test set of 1000 images.

## Conclusion
This project successfully addresses the challenge of digitizing handwritten answer scripts using deep learning techniques. Further improvements could be made by utilizing larger and more diverse datasets.

## Authors
- [Akriti Gupta](mailto:gupta.97@iitj.ac.in) (B.Tech. Artificial Intelligence & Data Science)
- [Sagnik Goswami](mailto:goswami.5@iitj.ac.in) (B.Tech. Artificial Intelligence & Data Science)  
- [Tanish Pagaria](mailto:pagaria.2@iitj.ac.in) (B.Tech. Artificial Intelligence & Data Science)
- [Uppala Giridhar](mailto:giridhar.1@iitj.ac.in) (B.Tech. Electrical Engineering)  

(IIT Jodhpur Undergraduates)