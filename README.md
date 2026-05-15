git clone https://github.com/2026bmtproject/tracknetv3-custom.git

cd tracknetv3-custom

python -m venv venv

source venv/bin/activate   # Windows: venv\Scripts\activate

pip install -r requirements.txt

Download  https://drive.google.com/file/d/1CfzE87a0f6LhBp0kniSl1-89zaLCZ8cA/view?usp=sharing
Unzip the file and place the parameter files to ckpts
unzip TrackNetV3_ckpts.zip
確保有ckpts/TrackNet_best.pt和ckpts/InpaintNet_best.pt

放一個test.mp4，幾秒就好電腦會炸

python predict.py --video_file test.mp4 --tracknet_file ckpts/TrackNet_best.pt --inpaintnet_file ckpts/InpaintNet_best.pt --save_dir prediction --output_video

python 3.12.5