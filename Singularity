
BootStrap:docker
From:tensorflow/tensorflow:1.0.1-gpu

%runscript
  exec python "$@" 

%post
  # Enables access to ACCRE storage
  mkdir /scratch /data /gpfs22 /gpfs23 /dors

%test
python -c "import tensorflow"
