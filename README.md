# Pixel-Play-25

## Description
This project implements a zero-shot learning image classifier to categorize images onto 50 classes without directly training them onto 10 hidden classes. It uses attribute embeddings to achive classification using semantic vector space.

## Features
- Zero-shot classiffication
- Use of Pre-trained EfficientNetb0 model

## Results
- Achieved an accuracy of 58% on Pixel-play train dataset.
- 99% on the the Special-Package.

## Insights
- Let the fraction of seen classes in test data set be x.
- Then the fraction of unseen classes will be (1-x).
- Special Package only contains samples from seen classses. Therefore, the accuracy on seem classes (a1) can be approximated as a1=100%.
- When I tried to get only unseen classes as output it yeilded me an accuracy of nearly 20% from all the test samples but as stated earlier we will use only unseen classes samples then the accuracy of unseen classes (a2) can be approximated as a2=20/(1-x).
- Total accuracy can be calculated as
              Total accuracy = a1*x + a2*(1-x).
- On solving x = 0.4
  **This means 60% of the test data was from unseen classes**

## Project Structure
- README.md file
- Codebase
- Output CSV's
- Predicate matrix CSV's

## Other Ideas
Use of meta learning and prototype learning for better results. I have studied their concepts but unable to implement them. Would love to implement them with team VLG

## Acknowledgements
- Studied few research papers related to zero- shot classification and the use of vector embeddings.
- Pre-trained EfficientNetb0 model
