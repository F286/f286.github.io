---
published: false
---
## Install CUDA (v8.0)

You might need to make an NVIDIA developer account to do this, it's free.

## Install Anaconda

I used the latest version.

## Create virtualenv (virtual environment) in Anaconda

Open the Anaconda command prompt and type these in, line by line. (copied from [here](http://www.heatonresearch.com/2017/01/01/tensorflow-windows-gpu.html))

# GPU version

`conda create --name tensorflow python=3.5
activate tensorflow
conda install jupyter
conda install scipy
pip install tensorflow`

# CPU version

`conda create --name tensorflow python=3.5
activate tensorflow
conda install jupyter
conda install scipy
pip install tensorflow`

## Use specific environment in PyCharm

Anaconda creates a virtual environment for the Python (I used community edition), you can set this in the Project Interperter page look for python.exe in the install directory. Anaconda created the virtual environment on my computer at _C:\ProgramData\Anaconda3\envs\tensorflow_, but this may vary.

## Extra stuff do do with CUDA

Thanks. This was the problem (I hadn't placed cudnn in the proper location) - I copied it into the nVidia CUDA install location. I downloaded Windows 7 Version cuDNN - incase other people are wondering.

I then copied the _cudnn645.dll (cuda\bin\cudnn645.dll)_ from that zip archive into _C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v8.0\bin\;_

_cuda\include\cudnn.h_ to _C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v8.0\include\;_

and

_cuda\lib\x64\cudnn.lib_ to _C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v8.0\lib\x64\_

WHERE _C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v8.0_ is my install PATH for the CUDA toolkit.

I had already added _C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v8.0\bin\ _to my **PATH** (you need to make sure this is done too).

## How to set path variable

It looks like this, change the right part to what it is on your computer.

`set PATH=%PATH%;C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v8.0\bin`
