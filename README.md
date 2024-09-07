# Simplistic benchmarking of GPT-4o-mini on the Fashion MNIST dataset

## Prompt
Prompt is
```
You are presented with a greyscale low-resolution image of a piece of clothing.
It is of one of the possible classes:
{LABELS_MESSAGE}

Your task is to classify the image into one of the classes.
Format your output like this:
First, reason about what features let you classify the image correctly. 
If there's some ambiguity - reason about it and try to come to the most probable conclusion. 
Your reasoning should be 2-4 sentences at max.
You last line should always be class label, nothing else

Your last line should always be a class label from the list above! If you are not sure - try to make your best guess. 
```

## Notes
GPT-4o-mini declined to classify 30 of the images. They are presented in `bad_imgs` folder
`results.csv` contains per-image classification results with LLM's reasoning

## Results
Accuracy: 0.8085
Classification Report:

              precision    recall  f1-score   support

           0       0.68      0.70      0.69      1000
           1       0.99      0.98      0.99      1000
           2       0.69      0.88      0.78      1000
           3       0.73      0.93      0.81      1000
           4       0.86      0.56      0.68      1000
           5       0.96      0.86      0.91      1000
           6       0.52      0.51      0.51      1000
           7       0.82      0.98      0.89      1000
           8       0.99      0.82      0.90      1000
           9       0.97      0.87      0.92      1000

    accuracy                           0.81     10000
    mcr avg        0.82      0.81      0.81     10000
    wghtd avg      0.82      0.81      0.81     10000

