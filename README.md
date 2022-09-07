# Introduction
How do you find out what guys are occupying your precious GPU resources? If you still just simply run `nvidia-smi` to get PIDs and use `ps` to inspect their owners one by one, then this tool is designed for you! A simple yet powerful python script that has no dependency at all!
# Usage
```
./nvidia-smi-userinfo
```
# Output example
```
+-----------------------------------------------------------------------------+
| NVIDIA-SMI 470.94       Driver Version: 470.94       CUDA Version: 11.4     |
|-------------------------------+----------------------+----------------------+
| GPU  Name        Persistence-M| Bus-Id        Disp.A | Volatile Uncorr. ECC |
| Fan  Temp  Perf  Pwr:Usage/Cap|         Memory-Usage | GPU-Util  Compute M. |
|                               |                      |               MIG M. |
|===============================+======================+======================|
|   0  NVIDIA GeForce ...  Off  | 00000000:01:00.0 Off |                  N/A |
| 40%   57C    P2   234W / 350W |  11931MiB / 12053MiB |     23%      Default |
|                               |                      |                  N/A |
+-------------------------------+----------------------+----------------------+
|   1  NVIDIA GeForce ...  Off  | 00000000:04:00.0 Off |                  N/A |
| 40%   56C    P2   245W / 350W |  11931MiB / 12053MiB |     69%      Default |
|                               |                      |                  N/A |
+-------------------------------+----------------------+----------------------+
|   2  NVIDIA GeForce ...  Off  | 00000000:05:00.0 Off |                  N/A |
| 40%   54C    P2   253W / 350W |  11931MiB / 12053MiB |     67%      Default |
|                               |                      |                  N/A |
+-------------------------------+----------------------+----------------------+
|   3  NVIDIA GeForce ...  Off  | 00000000:08:00.0 Off |                  N/A |
| 41%   57C    P2   231W / 350W |  11931MiB / 12053MiB |     27%      Default |
|                               |                      |                  N/A |
+-------------------------------+----------------------+----------------------+
|   4  NVIDIA GeForce ...  Off  | 00000000:09:00.0 Off |                  N/A |
| 40%   46C    P2   158W / 350W |   5357MiB / 12053MiB |      0%      Default |
|                               |                      |                  N/A |
+-------------------------------+----------------------+----------------------+
|   5  NVIDIA GeForce ...  Off  | 00000000:82:00.0 Off |                  N/A |
| 40%   36C    P8    19W / 350W |      2MiB / 12053MiB |      0%      Default |
|                               |                      |                  N/A |
+-------------------------------+----------------------+----------------------+
|   6  NVIDIA GeForce ...  Off  | 00000000:85:00.0 Off |                  N/A |
| 41%   36C    P8    20W / 350W |      2MiB / 12053MiB |      0%      Default |
|                               |                      |                  N/A |
+-------------------------------+----------------------+----------------------+
|   7  NVIDIA GeForce ...  Off  | 00000000:86:00.0 Off |                  N/A |
| 40%   35C    P8    20W / 350W |      2MiB / 12053MiB |      0%      Default |
|                               |                      |                  N/A |
+-------------------------------+----------------------+----------------------+
|   8  NVIDIA GeForce ...  Off  | 00000000:89:00.0 Off |                  N/A |
| 42%   40C    P8     8W / 350W |      2MiB / 12053MiB |      0%      Default |
|                               |                      |                  N/A |
+-------------------------------+----------------------+----------------------+
|   9  NVIDIA GeForce ...  Off  | 00000000:8A:00.0 Off |                  N/A |
|  0%   29C    P8    24W / 350W |      2MiB / 12053MiB |      0%      Default |
|                               |                      |                  N/A |
+-------------------------------+----------------------+----------------------+

+-----------------------------------------------------------------------------+
| Processes:                                                                  |
|  GPU   GI   CI        PID   Type   Process name                  GPU Memory |
|        ID   ID                                                   Usage      |
|=============================================================================|
|    0   N/A  N/A     13628      C   python                          11929MiB |
|    1   N/A  N/A     16352      C   python                          11929MiB |
|    2   N/A  N/A     17605      C   python                          11929MiB |
|    3   N/A  N/A     18149      C   python                          11929MiB |
|    4   N/A  N/A      9590      C   python                           5355MiB |
+-----------------------------------------------------------------------------+

GPU: 0          PID: 13628              USER: <USER A>
GPU: 1          PID: 16352              USER: <USER A>
GPU: 2          PID: 17605              USER: <USER A>
GPU: 3          PID: 18149              USER: <USER A>
GPU: 4          PID: 9590               USER: <USER B>
```
