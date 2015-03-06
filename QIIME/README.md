Make sure you have docker daemon run on it

Build :
sudo docker build -t ubuntu-qiime:v01 .

Example:
sudo docker run -it ubuntu-qiime:v01 /bin/bash


you will see a bash prompt inside docker container, run "print_qiime_config.py -t" will invoke testing
