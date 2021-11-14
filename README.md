# IS5452 - Emergency Dispatcher Assistance System (EDAS) - Team 7
## Project Structure
 ``` 
.
├── README.md
├── base-model.ipynb # train model
├── emotion-gender.ipynb # evaluation with gender
├── emotion-without_gender.ipynb # evaluation without gender
├── gender100.pth # pretrain model with gender 
├── 100.pth # pretrain model without gender 
└── testdata
 ``` 
## Prerequisites
- python3
- librosa
- numpy
- torch
- sklearn
- pandas
## Getting Start
For dataset, you could download RAVDESS or use records in testdata to test code.
### Training model
Modify the path in ` /base-model.ipynb` , change the path in [] into the path where you download the dataset.
``` 
path ='[../input/ravdess/RAVDESS]'
...
file_path.append('[../input/ravdess/RAVDESS/]' + file)
``` 
You could change the training epoch in ` /base-model.ipynb` 
``` 
for epoch in range(1,60):
``` 
### Test on no gender input
For dataset, you could download RAVDESS or use records in testdata to test code.
### Training model
Modify the path in ` /emotion-without_gender.ipynb` or ` /emotion-gender.ipynb` , change the path in [] into the path where you download the dataset.
``` 
path ='[../input/ravdess/RAVDESS]'
...
file_path.append('[../input/ravdess/RAVDESS/]' + file)
``` 
You could change the training epoch in ` /emotion-without_gender.ipynb` or ` /emotion-gender.ipynb`
``` 
for epoch in range(1,100):
``` 
In this files, output of confusiom matrix, classification report and emotion count report are all saved. Or if you want to retest, just run the files.
