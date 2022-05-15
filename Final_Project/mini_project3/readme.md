We changed our direction from our mini-project 2, which was about Fast-speech2.

In mini-project3, Tacotron2 is our main subject. This repository includes following files in a table below:


File Name | Description
------------- | -------------
mini_project3.ipynb | Main code file 
tacotron2_layer.py  | Where we updated hyper-param
tacotron2_model.py  | model.py file
encode_model2.wav   | Modified encode model sample output file



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
      --out_path "/content/drive/MyDrive/output/model##.wav"
```





