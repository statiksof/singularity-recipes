bootstrap: docker
From: ubuntu:18.04

%post
    # update and install pip
    apt-get -y update
    apt-get -y install python3-pip

    # update pip and install jupyter
    pip3 install --upgrade pip
    pip3 install jupyter

    # clean apt
    apt-get autoremove -y
    apt-get clean

%runscript
    echo "Starting the notebook ..."
    echo "Open browser to localhost:8888"
    exec /usr/local/bin/jupyter notebook --ip='*' --port=8888 --no-browser