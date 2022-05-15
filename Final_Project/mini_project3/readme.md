We changed our direction from our mini-project 2, which was about Fast-speech2.

In mini-project3, Tacotron2 is our project. This repository includes following files in a table below:


File Name | Description
------------- | -------------
mini_project3.ipynb  | Content Cell
Content Cell  | Content Cell



a. First download git and install requirement.txt


```
!git clone https://github.com/coqui-ai/TTS
```
```
!pip install -r /TTS/requirements.txt
```


b. install relevant packages 

```
!pip install -e .[all,dev,notebooks] 
!pip install numpy==1.21.5
!pip install pandas
```

c. The dataset can be found at https://data.keithito.com/data/speech/LJSpeech-1.1.tar.bz2 : We will skip the process of how to unzip the file as it was already mentioned in mini-project2. 


d. Run the pretrained model
```
!CUDA_VISIBLE_DEVICES="0" python /content/drive/MyDrive/TTS/train_tacotron_ddc.py
```
e. saving output

```
!tts --text "3 epochs yay" \
      --model_path "/content/drive/MyDrive/TTS/recipes/ljspeech/tacotron2-DDC/run-May-14-2022_09+02PM-0000000/best_model_6090.pth" \
      --config_path "/content/drive/MyDrive/TTS/recipes/ljspeech/tacotron2-DDC/run-May-14-2022_09+02PM-0000000/config.json" \
      --out_path "/content/drive/MyDrive/output/model2.wav"
```





![image](https://user-images.githubusercontent.com/71423299/164359823-6d5604c6-9e0e-4f46-a696-2cf400bcd492.png)



## We saved the sample output 
Sample output files: 
* The cat is jumping on the ball and making silly noises.wav
* This is Badri, Swapan, and Geonwoo and this is a sample output file we generated using fast speech .wav

Synthetized Spectrogram picture for The Cat is jumping file below:
![The cat is jumping on the ball and making silly noises](https://user-images.githubusercontent.com/71423299/164358203-ff250893-661f-4f28-9d37-2c1f6161fa0f.png)
