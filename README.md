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

- Download pretrained models to pre_trained :
   1. [places](https://drive.google.com/file/d/1ARP8GS5LMGYc8T8lFTuYkBl9I9kJoIiL/view)
   2. [emotion](https://drive.google.com/file/d/1sWx3ze8XfZEGf-kPcmiYpY9EOzugdzgu/view)
 
- Extract image features: python feature_extraction/extract_img_feats.py --vtype imagenet --mvsa single --ht False
- Extract text features: python feature_extraction/extract_txt_feats.py --btype robertabase --mvsa single --ht True

- For Extract multimodal features  MM_Feature_Extraction.ipynb

(It produces a file in .json format in the ./features folder.)

## Train and Evaulate Models


1. For **CLIP** model for Image and Text: MM_CLIP+CLIP.ipynb

2. For training using **CLIP** model for Image and **RoBERTa** model for Text: MM_CLIP+Roberta: MM_CLIP+Roberta.ipynb

3. To train using **ResNet**  Model trained on ImageNet dataset for Image and **RoBERTa**  for Text: MM_ResNet+Roberta.ipynb

## Test MultiModal

For testing multimodal model from image and text data pair MM_Predict.ipynb
