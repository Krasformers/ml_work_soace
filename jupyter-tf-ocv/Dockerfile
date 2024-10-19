FROM tensorflow/tensorflow:latest-gpu
COPY requirements.txt /requirements.txt
RUN  apt-get -y update && apt-get -y full-upgrade
RUN  apt-get -y install python3-pip
RUN  python3 -m pip install --upgrade pip
RUN  python3 -m pip install -r /requirements.txt --no-cache-dir --root-user-action=ignore
RUN apt-get -y install python3-opencv
WORKDIR /tf
CMD  jupyter notebook --notebook-dir="/tf/notebooks" --ip=0.0.0.0 --port=8888 --no-browser --allow-root