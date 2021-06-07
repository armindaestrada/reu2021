Dockers Installation
++++++++++++++++++++++
Before installing Dockers, create a `Docker Hub Account <https://hub.docker.com/signup>`_

Ubuntu 20.04 
-----------------
You may also visit their official site `Install Docker Engine on Ubuntu <https://docs.docker.com/engine/install/ubuntu/>`_ for more details.

Set up the repository
    Update the apt package index and install packages to allow apt to use a repository over HTTPS.
    ::
        sudo apt-get update
        sudo apt-get install \
        apt-transport-https \
        ca-certificates \
        curl \
        gnupg \
        lsb-release

    Add Docker's offical GPG key: 
    ::
        curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg

    Use the following command to set up the stable repository. 
    ::
        echo \
        "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
        $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

Install Docker Engine
    Update the apt package index, and install the latest version of Docker Engine and containerd, or go to the next step to install a specific version:
    ::
        sudo apt-get update
        sudo apt-get install docker-ce docker-ce-cli containerd.io
    
    Add your username to a docker group and add the user to the docker group. This will be needed in order to run ``Dockers`` without having to type ``sudo`` every time at the beginning of a command. 
    ::
        sudo groupadd docker
        sudo usermod -aG docker $USER

**Close your current terminal and open a new one.**

    Verify that Docker Engine is installed correctly by running the hello-world image.
    ::
        docker run hello-world

    .. note:: If you still get a ``permission denied`` error , use the following command to activate the changes to the group. 
        ::
            newgrp docker 

    Verify that the image is up and running
    ::
        docker images

Windows 10 
-----------
1. Download installer from `Install Docker Desktop on Windows <https://docs.docker.com/docker-for-windows/install/>`_
2. Open and click ``ok`` on the configuation window to install Docker Desktop. 
3. Once all the packages have upacked, click on ``Close and restart``. This will restart your computer. 
4. Verify that Docker Engine is installed correctly by running the hello-world image, open a ``command prompt`` window and run 
::
    docker run hello-world
5. To verify the image is up and running
::
    docker images

MacOS
--------
1. Download installer from `Install Docker Desktop on Mac <https://docs.docker.com/docker-for-mac/install/>`_
2. Open the installer once downloaded and drag the icon to the applications folder as prompted. This will take several minutes. 
3. On the other pop-up click on ``open Docker``. 
4. A Verifying "Docker"... pop-up will take several minutes. 
5. Go to your applications and open ``Docker``. 
6. You will get a message that states the app has been downloaded from the internet. Select ``open``. 
7. Give Docker Destop priviledged access (It will ask for your password). 
8. Give it a few minutes for the Docker Engine to Initiate. On your status bar you will see the Docker icon initiating. 
9. You will see a "No containers running" message. 
10. Click on the copy icon to copy the code and run it on a terminal window. It should look something like this. 
    ::
        docker run -d -p 80:80 docker/getting-started
11. Return to the Docker Desktop Engine and you will see that there is a container.
12. Verify that the Docker Engine is installed correctly on your terminal run: 
    ::
        docker run hello-world
13. To verify the image is up and running
    ::
        docker images
