# nvidia-profiler
Commands to use the nvidia profiler, nsight systems and nsight compute.

## Source env variables
```
export CUDA_HOME=/usr/local/cuda
export PATH=${CUDA_HOME}/bin:${PATH}
export LD_LIBRARY_PATH=${CUDA_HOME}/lib64:$LD_LIBRARY_PATH
```

## Check status
```
nsys status -e
```


## Nvidia Nsight Systems
```
nsys profile --stats=true python main.py
nsys profile –t cuda,osrt,nvtx –o baseline –w true python main.py
```

## Nvidia Nsight Compute
```
ncu -o profile  python main.py
ncu -o profile --set full
```

