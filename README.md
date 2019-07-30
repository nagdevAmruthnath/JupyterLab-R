# JupyterLab-R
![alt text](https://github.com/nagdevAmruthnath/JupyterLab-R/blob/master/jp.JPG)
This repository contains a dockerfile for Jupyterlab and R kernal for performing notebook style analysis. This dockerfile also containes essesntial R-packages for machine and deep learning such as caret, h2o, dplyr and devtools for pulling packages from git repos. 

## Building docker image from this repository
To build this dockerimage straight from the repository, you first need to curl to pull the dockerfile and then build the dockerfile in this repos as follows  

`curl https://raw.githubusercontent.com/nagdevAmruthnath/JupyterLab-R/master/dockerfile > ./df && sudo docker build -t df .`

## Running the docker image
By default, jupyter lab run on port 8888 and this dockerfile is customized to remove any tokens or passwords. This directly loads up the instance. To run this image use the following command in your terminal.

`sudo docker run -ti -p 0.0.0.0:8888:8888 df:latest`  
You can also attach volumes to this and you can find the documentation [here](https://docs.docker.com/engine/reference/commandline/volume_create/). 

