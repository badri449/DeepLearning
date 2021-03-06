This mini-project 2 repository. For mini-project3, Please go to mini_project3 directory. 

This is a PyTorch implementation of Microsoft's text-to-speech system FastSpeech 2: Fast and High-Quality End-to-End Text to Speech. This project is based on xcmyz's implementation of FastSpeech. 

Currently we are working on 
* How the code is working 
* If the code can generate desirable output 

a. First download git and install requirement.txt


```
!git clone https://github.com/ming024/FastSpeech2 
```
```
!pip install -r ./fastspeech2_hf/requirements.txt
```


b. install relevant packages 

```
!pip3 install PyYAML==5.4.1
!pip3 install g2p-en==2.1.0
!pip3 install pypinyin==0.39.0
!pip3 install unidecode==1.1.1
```
c. Create directories on FastSpeech2 to save output generated from running model on step d. 
```
FastSpeech2/output/result/LJSpeech
```


d. You have to download [the pretrained models](https://drive.google.com/drive/folders/1DOhZGlTLMbbAAFZmZGDdc77kz1PloS7F?usp=sharing) and put them in output/ckpt/LJSpeech/
* we chose LSpeech_900000.zip

e. Run the model

```
!python3 synthesize.py --text "This is Badri, Swapan, and Geonwoo and this is a sample output file we generated using fast speech  " --restore_step 900000 --mode single -p config/LJSpeech/preprocess.yaml -m config/LJSpeech/model.yaml -t config/LJSpeech/train.yaml
```
There is a chance you encounter an error then you have to unzip these two files 

![image](https://user-images.githubusercontent.com/71423299/164359823-6d5604c6-9e0e-4f46-a696-2cf400bcd492.png)



## We saved the sample output 
Sample output files: 
* The cat is jumping on the ball and making silly noises.wav
* This is Badri, Swapan, and Geonwoo and this is a sample output file we generated using fast speech .wav

Synthetized Spectrogram picture for The Cat is jumping file below:
![The cat is jumping on the ball and making silly noises](https://user-images.githubusercontent.com/71423299/164358203-ff250893-661f-4f28-9d37-2c1f6161fa0f.png)
