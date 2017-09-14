
BootStrap:docker
From:tensorflow/tensorflow:1.3.0-gpu

%runscript
  exec cat /etc/issue

%post
  # Enables access to ACCRE storage
  mkdir /scratch /data /gpfs22 /gpfs23 /dors

  add-apt-repository ppa:jonathonf/ffmpeg-3
    
  apt update && \
    apt install -y \
      ffmpeg \
      libav-tools \
      x264 \
      x265 \
      python-tk
        
  pip install \
    librosa==0.5.1 \
    pandas==0.20.3 \
    scikit-learn==0.18.1 \
    seaborn==0.8.1

%test
  python -V
  python -c "import librosa; import pandas; import sklearn; import seaborn"
