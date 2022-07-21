# Quick Start

## Requirements

To get started, the following requirements should be fulfilled.

- **Python** Python3.7 or higher version is required for full functions.

## Installation 

First, download OpenBlimp github to your local folder if you haven’t done it. To clone repository:

```powershell
git clone https://github.com/zhz03/OpenBlimp.git
cd OpenBlimp
```

Make sure you are in the root dir of OpenCDA, and next let’s install the dependencies. **We highly recommend use conda environment to install.**

```powershell
conda env create -f environment.yml
conda activate openblimp
```

If conda install failed, install through pip:

```
pip install -r requirements.txt
```

## Code Structure

```
root
├───docs
│   ├───Demo
│   └───javascripts
├───Hardware
│   ├───3d_design
│   │   └───origami structure
│   ├───circuit_plot_doc
│   └───Images
│       ├───assembly
│       ├───cases
│       ├───motor_propellers
│       ├───prepare
│       └───sensors
├───imgs
└───openblimp
    ├───auto_control
    ├───basic_control
    ├───Images
    │   └───communication
    └───manual_control
        └───arduino_code
```

Note:

- `Hardware` directory contains all the hardware files like: 3D design files, hardware images, other hardware related files
- `openblimp` directory contains all the software files and code. 