# nvidia-profiler

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

ncu-ui profile.ncu-rep

