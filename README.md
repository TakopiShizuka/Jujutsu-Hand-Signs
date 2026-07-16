# Jujutsu-Hand-Signs
This project helps people who are fans of Jujutsu Kaisen to learn the different hand signals of many characters. It also serves an entertainment purpose for people who want to practice their skills and show their dedication to the anime through practicing hand signs.
I used image net and downloaded a data set from (https://universe.roboflow.com/) and searched for a dataset for jujutsu hand signals and then I trained the model to recognize different hand signals from the data set.

Steps
I copied the c-url of the data set I found
Then I used the following commands in the terminal:

cd  jetson-inference/python/training/classification/data

wget https://nvidia.box.com/shared/static/o577zd8yp3lmxf5zhm38svrbrv45am3y.gz -O jjk.tar.gz

tar xvzf jjk.tar.gz

cd ~/jetson-inference

./docker/run.sh

cd python/training/classification

python3 train.py --model-dir=models/jjk data/jjk

python3 onnx_export.py --model-dir=models/jjk


NET=models/jjk
DATASET=data/jjk
