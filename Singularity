
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
      python3 \
      python-tk
        
  pip install --upgrade \
    librosa \
    pandas \
    scikit-learn \
    seaborn \
    matplotlib \
    scipy \
    numpy \
    jupyter \
    keras
    

%test
  python -V
  python -c "import librosa; import pandas; import sklearn; import seaborn"
