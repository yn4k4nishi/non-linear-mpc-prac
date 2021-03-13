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
    osバージョンが19042.867で 20145以上じゃないのが原因
