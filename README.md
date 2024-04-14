Windows
1.Install GPU-Z_ASUS_ROG_2.58.0.exe and check CUDA available

2, 
https://www.tensorflow.org/install/source#gpu
Requirement:
tensorflow-2.6.0
3.6-3.9	GCC 7.3.1
Bazel 3.7.2
cvDNN: 8.1
CUDA :11.2

CUDA :https://developer.nvidia.com/cuda-toolkit-archive
cuDNN: https://developer.nvidia.com/rdp/cudnn-archive

kiểm tra GPU NVIDIA có phù hợp với Tensorflow và CUDA không?
Giả sử bạn có GPU NVIDIA GTX 660, tìm trong trang https://developer.nvidia.com/cuda-gpus được kết quả Compute Capability là 3.0 như hình dưới
Theo hardware requirement của Tensorflow thì support 3.5 trở lên, do đó GTX 660 không thể chạy được Tensorflow GPU

3,Cài đặt CUDA
4,Cài đặt cuDNN
5,Cài đặt package tensorflow-gpu
pip install tensorflow-gpu==2.6.0
import tensorflow as tf
tf.test.is_built_with_cuda()
tf.config.list_physical_devices('GPU')