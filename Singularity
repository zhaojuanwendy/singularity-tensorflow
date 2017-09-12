
BootStrap:docker
From:tensorflow/tensorflow:1.3.0-gpu

%runscript
  exec cat /etc/issue

%post
  # Enables access to ACCRE storage
  mkdir /scratch /data /gpfs22 /gpfs23 /dors

  
  pip install librosa==0.5.1

%test
  python -V
  python -c "import librosa"
