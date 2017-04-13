# Initial steps: medical automatic speech recognition

After downloading this repo, do the following steps:  
```
./scripts/install.sh
``` 
To set the environment variables:  
```
source ~/.bashrc
``` 
Then download the data:  
```
./download.sh
``` 
Convert flac to wav:  
```
./flac_to_wav.sh /path/to/LibriSpeech
``` 
Create json description files:  
```bash
$python create_desc_file.py /path/to/LibriSpeech/train-clean-100 train_corpus.json
$python create_desc_file.py /path/to/LibriSpeech/dev-clean validation_corpus.json
$python create_desc_file.py /path/to/LibriSpeech/test-clean test_corpus.json
```
Try training:  
```bash
mkdir Models
$python train.py train_corpus.json validation_corpus.json Models/model1
```
