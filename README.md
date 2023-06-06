# openpai-testcase
用于openpai平台的测试用例  
openpai提供的镜像torch版本较低, 因此自制了一个支持GPU的镜像环境, 版本较新应该能支持大部分torch1.x的模型  
`docker pull nightwang/openpai_testcase:ubuntu20.04_pytorch1.12_cuda11.3`  
  
### Distribute
#### MNIST
**简介**: 图片识别小模型, 数据量很小, 用于环境测试.  
**Dockerfile**:  
`models/MNIST/Dockerfile.MNIST`  
**DockerHub**:  
`docker pull nightwang/openpai_testcase:ubuntu20.04_pytorch1.12_cuda11.3`  
**任务提交配置**:  
`models/MNIST/MNIST-DDP-nccl.yaml`  
注: worker执行的commands中参数-n和-g要和前面配置的instance数和gpu数对应  