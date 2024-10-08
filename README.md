# 安裝指南

## 環境

### 1. Anaconda
使用anaconda 建構新環境，python版本為`3.10.14`

### 2. 安裝SMAC
懶人版
```bash
pip install git+https://github.com/gingkg/smac.git
```
原始安裝
```bash
git clone https://github.com/gingkg/smac.git
pip install smac/
```

### 3. 安裝CUDA 11.7
https://developer.nvidia.com/cuda-11-7-0-download-archive

### 4. 安裝pytorch 1.X
```bash
pip install torch==1.13.1+cu117 torchvision==0.14.1+cu117 torchaudio==0.13.1 --extra-index-url https://download.pytorch.org/whl/cu117
```

### 5. 安裝星海爭霸II主程式
使用暴雪官方登入器安裝
https://tw.shop.battle.net/zh-tw

### 6. 下載pymarl主程式
``` bash
git clone https://github.com/gingkg/pymarl.git
```

### 7. 安裝其他依賴項
```bash
pip install sacred pyyaml tensorboard_logger cloudpickle protobuf==3.20.1
```

### 8. 下載SMAC地圖至StarCraft資料夾
地圖下載https://github.com/oxwhirl/smac/releases/tag/v1

放入`~/StarCraft II/Maps/`

### 9. 更改Numpy和scipy版本
因為原本的版本太新(我看是numpy-1.26.4)，會出現`module 'numpy' has no attribute 'bool'.`，

而scipy 1.14.1需要numpy<2.3,>=1.23.5
```bash
python -m pip uninstall numpy scipy
python -m pip install numpy==1.23.1 scipy==1.13
```
