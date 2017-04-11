---
published: true
---
## Install CUDA (v8.0)

Download [here](https://developer.nvidia.com/cuda-downloads). You might need to make an NVIDIA developer account to do this, it's free. 

## Install Anaconda

Download the latest version [here](https://www.continuum.io/downloads).

## Create virtualenv (virtual environment) in Anaconda

Open the Anaconda command prompt and type these in, line by line. (copied from [here](http://www.heatonresearch.com/2017/01/01/tensorflow-windows-gpu.html))

### GPU version

`conda create --name tensorflow python=3.5`

`activate tensorflow`

`conda install jupyter`

`conda install scipy`

`pip install tensorflow-gpu`

### CPU version

`conda create --name tensorflow python=3.5`

`activate tensorflow`

`conda install jupyter`

`conda install scipy`

`pip install tensorflow`

## Setup IDE

Anaconda creates a virtual environment (_virtualenv_) for the Python but that just like dlls and stuff used to build the project, you will need an IDE to write the python. It might be possible on command line too but that's painfun : ) For the IDE I'm using **PyCharm**, there's a free Community Edition that works fine. Create a new Project in PyCharm and then goto Help/Find Action.. and type _Project Interpreter_ and press Enter. Click the little gear at the top right and press **Add Local**, navigate to where Anaconda installed the _virtualenv_ on you computer and find the _python.exe_ file and press OK. 

On my computer the _virtualenv_ was located at _C:\ProgramData\Anaconda3\envs\tensorflow_

## Extra stuff do do with CUDA

https://developer.nvidia.com/rdp/cudnn-download

Download cuDNN v5.1 (Jan 20, 2017), for CUDA 8.0 ?

Thanks. This was the problem (I hadn't placed cudnn in the proper location) - I copied it into the nVidia CUDA install location. I downloaded Windows 7 Version cuDNN - incase other people are wondering.

The directories line up with the downloaded cuDNN thing and the CUDA Install folder, so copy the contents of the cuDNN zip into the CUDA install folder.

I then copied the _cudnn645.dll (cuda\bin\cudnn645.dll)_ from that zip archive into _C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v8.0\bin\;_

_cuda\include\cudnn.h_ to _C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v8.0\include\;_

and

_cuda\lib\x64\cudnn.lib_ to _C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v8.0\lib\x64\_

WHERE _C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v8.0_ is my install PATH for the CUDA toolkit.

I had already added _C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v8.0\bin\ _to my **PATH** (you need to make sure this is done too).

## How to set path variable

It looks like this, change the right part to what it is on your computer.

`set PATH=%PATH%;C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v8.0\bin`

## Relogin to Anaconda Prompt

Type this into console to 'log back into' virtual environment if you close the Anaconda Prompt. You may have to right click and _Open as Administrator_ for it to work properly.

`activate tensorflow`

## How to install Keras (additional)

Instructions from [here](http://stackoverflow.com/questions/34097988/how-do-i-install-keras-and-theano-in-anaconda-python-2-7-on-windows).

Install TDM GCC x64.

Install Anaconda x64.

Open the Anaconda prompt (Run as Administrator)

`conda update conda`

`conda update --all`

`conda install mingw libpython`

### Install the latest version of Theano and Keras

`pip install git+git://github.com/Theano/Theano.git`

`pip install git+git://github.com/fchollet/keras.git`

## Additional Dependencies

Depending on what libraries that you use you may need to install some extra packages, this can be eaisly done by opening the _Anaconda Prompt_, logging into your virtual environment, and installing the package.

`pip install matplotlib`

`conda install Pillow`

## Show TensorBoard

Goto Anaconda prompt, 'activate tensorflow' (or specific virtual environment that you are using), then navigate to the project directory on disk. Remember that just _D:_ will navigate you to a drive on windows.

Type this

tensorboard --logdir=facades_train

Then goto the URL it shows in a browser, such as this.

http://192.168.1.179:6006