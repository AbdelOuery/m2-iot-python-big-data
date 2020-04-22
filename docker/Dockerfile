RUN apt-get update  && \
    apt-get -y install curl && \
    apt-get install -qy python3 && \
    apt-get install -qy python3-pip && \
    apt-get install -qy vim && \
    apt-get -y install git

# Clone git repo
RUN git clone https://github.com/AbdelOuery/m2-iot-python-big-data/

WORKDIR /docker
ADD . /workspace
WORKDIR /workspace

RUN pip3 install jupyter

# Expoe 8000 Port
EXPOSE 8000

# Go to workspace
# CMD workspace --port 8000
CMD ["jupyter", "notebook", "--port=8888", "--no-browser", "--ip=0.0.0.0", "--allow-root"]
