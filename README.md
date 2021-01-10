
[![Build Status](https://travis-ci.org/martinkersner/gtop.svg?branch=master)](https://travis-ci.org/marmtinkersner/gtop)

# gtop for Jetson AGX Xavier
Mandeep Singh, 2021.
Modified from https://github.com/martinkersner/gtop, which is the original and for TX1 & TX2.

## Description
`gtop` is CPU, GPU and memory viewer utilizing information provided by `tegrastats` (terminal utility for [NVIDIA<sup>&reg;</sup> JETSON<sup>&trade;</sup>](http://www.nvidia.com/object/embedded-systems-dev-kits-modules.html) embedded platform). It requires `ncurses` and its output resembles [`htop`](https://github.com/hishamhm/htop).


The GPU % utilization is not clear from tegrastats so just report the number after 'GR3D_FREQ' that appears in tegrastats.

If CPU & GPU memory utilization can be figured out from the unified memory it will be great and can be added to this utility easily.

## Prerequisites

```
sudo apt-get install libncurses5-dev libncursesw5-dev
```

## Installation instruction
```
https://github.com/mink007/gtop_for_agx_xavier.git
cd gtop_for_agx_xavier
make
sudo ./gtop
```

It is recommended to create alias for `gtop` so it can be used from any directory. Add following line to your *.bashrc* file
```
alias gtop="sudo ./$PATH_TO_GTOP_DIRECTORY/gtop"
```
 and don't forget to replace `$PATH_TO_GTOP_DIRECTORY`.

## License

GNU General Public License, version 3 (GPL-3.0)
