# tensorflow_on_azure
Fixes to outdated instructions from Microsoft on installing Tensofflow on Azure

## Why: 


The directions posted here: 
https://blogs.msdn.microsoft.com/uk_faculty_connection/2017/03/27/azure-gpu-tensorflow-step-by-step-setup/
don't quite work out of the box for 2 reasons.

1. Where it recommends 
```
git clone https://github.com/leestott/Azure-GPU-Setup.git
cd azure-gpu-setup
```
those steps fail because of case-sensitive directory names. 

2. Where it recommends:
```
./gpu-setup-part2.sh
```
It requires a NVidia account which is a rather annoying requirement.
Instead, following the instructions here:
  https://developer.nvidia.com/cuda-downloads
the following works without a NVidia account
```
  wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1604/x86_64/cuda-repo-ubuntu1604_8.0.61-1_amd64.deb
  sudo dpkg -i cuda-repo-ubuntu1604_8.0.61-1_amd64.deb
```

3. The tensorflow instructions( https://www.tensorflow.org/install/install_linux ) make a reasonable case for recommending virtualenv.
