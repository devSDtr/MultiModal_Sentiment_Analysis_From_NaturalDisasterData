# MultiModal_Sentiment_Analysis_From_NaturalDisasterData
 Multi Modal Sentiment Analysis From Natural Disaster Images and Texts on Social Media.

This study represents a study examining the multimodal sentiment analysis of content shared on social media platforms.

## Data

The data includes 1,000 images and 1,000 texts on the theme of natural disasters from Twitter.

Available at : [https://drive.google.com/drive/folders/1TSmHiFRFWJiGQKy3WYArOvuOFCvao-q5?usp=sharing](https://drive.google.com/drive/folders/1TSmHiFRFWJiGQKy3WYArOvuOFCvao-q5?usp=sharing)

valid_pairlist.txt format is file_id (filename), multimodal label, text label, image label

| Data Label   | Sentiment  |
|:-------:| -----:|
| 0       | Neutral    |
| 1       | Positive   |
| 2       | Negative   |

## Extract Features

For Extract multimodal features  MM_Feature_Extraction.ipynb

## Train and Evaulate Models


1. For **CLIP** model for Image and Text: MM_CLIP+CLIP.ipynb

2. For training using **CLIP** model for Image and **RoBERTa** model for Text: MM_CLIP+Roberta: MM_CLIP+Roberta.ipynb

3. To train using **ResNet**  Model trained on ImageNet dataset for Image and **RoBERTa**  for Text: MM_ResNet+Roberta.ipynb

## Test MultiModal

For testing multimodal model from image and text data pair MM_Predict.ipynb
