# glSpecializeShader segfaults

```
$ nvidia-smi
Tue Oct 20 13:52:17 2020       
+-----------------------------------------------------------------------------+
| NVIDIA-SMI 455.26.01    Driver Version: 455.26.01    CUDA Version: 11.1     |
|-------------------------------+----------------------+----------------------+
| GPU  Name        Persistence-M| Bus-Id        Disp.A | Volatile Uncorr. ECC |
| Fan  Temp  Perf  Pwr:Usage/Cap|         Memory-Usage | GPU-Util  Compute M. |
|                               |                      |               MIG M. |
|===============================+======================+======================|
|   0  GeForce RTX 2060    Off  | 00000000:01:00.0  On |                  N/A |
| 32%   37C    P8    21W / 160W |    497MiB /  5931MiB |     20%      Default |
|                               |                      |                  N/A |
+-------------------------------+----------------------+----------------------+
                                                                               
+-----------------------------------------------------------------------------+
| Processes:                                                                  |
|  GPU   GI   CI        PID   Type   Process name                  GPU Memory |
|        ID   ID                                                   Usage      |
|=============================================================================|
|    0   N/A  N/A      1190      G   /usr/lib/xorg/Xorg                333MiB |
|    0   N/A  N/A      2548      G   ...AAAAAAAAA= --shared-files      140MiB |
+-----------------------------------------------------------------------------+


$ clang++ segfault.cxx -lGL -lgl3w -lglfw -o segfault
$ ./segfault
Loading shader _Z9frag_mainI11devil_egg_tEvv from shadertoy.cxx.spv
Segmentation fault (core dumped)
```


