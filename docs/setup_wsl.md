## CUDA on WSL
https://docs.nvidia.com/cuda/wsl-user-guide/index.html

- Windows Insider Program から最新をインストール
- WindowsにNVIDIAのドライバーをインストール
- WSL2のインストール

- CUDA Toolkitのセットアップ
```bash
$ sudo apt-key adv --fetch-keys http://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64/7fa2af80.pub
$ sudo sh -c 'echo "deb http://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64 /" > /etc/apt/sources.list.d/cuda.list'
$ sudo apt update 
$ sudo apt install -y cuda-toolkit-11-0
```

- サンプルの実行
    - `/usr/loca/cuda/samples`以下で`sudo make`を実行
    - `./bin/x86_64/linux/releaseBlackScholes`
    > CUDA error at ../../common/inc/helper_cuda.h:777 code=35(cudaErrorInsufficientDriver) "cudaGetDeviceCount(&device_count)" 
        - osバージョンが19042.867で 20145以上じゃないのが原因
        - wsl2ではなくwsl1なのも原因
    > [./BlackScholes] - Starting...
GPU Device 0: "Turing" with compute capability 7.5

Initializing data...
...allocating CPU memory for options.
...allocating GPU memory for options.
...generating input data in CPU mem.
...copying input data to GPU mem.
Data init done.

Executing Black-Scholes GPU kernel (512 iterations)...
Options count             : 8000000     
BlackScholesGPU() time    : 0.501742 msec
Effective memory bandwidth: 159.444437 GB/s
Gigaoptions per second    : 15.944444     

BlackScholes, Throughput = 15.9444 GOptions/s, Time = 0.00050 s, Size = 8000000 options, NumDevsUsed = 1, Workgroup = 128

Reading back GPU results...
Checking the results...
...running CPU calculations.

Comparing the results...
L1 norm: 1.741792E-07
Max absolute error: 1.192093E-05

Shutting down...
...releasing GPU memory.
...releasing CPU memory.
Shutdown done.

[BlackScholes] - Test Summary

NOTE: The CUDA Samples are not meant for performance measurements. Results may vary when GPU Boost is enabled.

Test passed
