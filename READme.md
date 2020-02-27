Windows 10
step 1: Change anyother mode to "Developer mode"
goto Update and Security -> For Developer -> "Developer mode"

step 2:
goto 
Control Panel\All Control Panel Items\Programs and Features

step 3:
enable "Windows subsystem for Linux" feature and Restart the system

step 4:
goto Microsoft Store to install "ubuntu" software 

step 5:
start ubuntu terminal in windows to set user name and password

step 6: update and upgrade your ubuntu terminal
sudo apt-get update
sudo apt-get upgrade

step 7: install python3, pip3
sudo apt-get install python3
sudo apt-get install python3-pip

step 8: change directory [c disk or any disk partitions]
ls /mnt/
cd /mnt/d

mkdir DeepSpeech
cd DeepSpeech

step 9: install virtualenv
sudo apt-get install virtualenv
pip3 install virtualenv

step 10: Create and Activate Virtual Environment
virtualenv --python=python3 env
source env/bin/activate

step 11: Download pre-trained English model and extract
curl -LO https://github.com/mozilla/DeepSpeech/releases/download/v0.6.1/deepspeech-0.6.1-models.tar.gz
tar xvf deepspeech-0.6.1-models.tar.gz

step 12: Download example audio files
curl -LO https://github.com/mozilla/DeepSpeech/releases/download/v0.6.1/audio-0.6.1.tar.gz
tar xvf audio-0.6.1.tar.gz

step 13: install deepspeech via pip
pip3 install deepspeech=0.6.1 

step 14: test the inference results"
deepspeech --model deepspeech-0.6.1-models/output_graph.pbmm --lm deepspeech-0.6.1-models/lm.binary --trie deepspeech-0.6.1-models/trie --audio audio/2830-3980-0043.wav 

step 15: Realtime application
git clone https://github.com/mozilla/DeepSpeech-examples.git
cd DeepSpeech-examples/vad_transcriber

change deepspeech version whatever you want

pip3 install -r requirements.txt

if you getting error, try this
pip3 uninstall pyqt5
sudo apt install python3-pyqt5
export PYTHONPATH=/usr/lib/python3/dist-packages/
