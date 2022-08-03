# Quick Start

Building a blimp from scratch is not easy, but with our quick start. You can easily build your own blimp.

## Step 1: Build your blimp

To quickly build your own blimp: 

- Purchase the off-the-shelf balloon that we are most recommended: [Remote Control Shark Toy Inflatable Air Shark Balloon RC Blimp Fish Toy](https://www.amazon.com/Remote-Control-Inflatable-Balloon-Decoration/dp/B0B5MZ8L23/ref=sr_1_10?crid=182ZKFN0U0DE2&keywords=shark+fish+balloon&qid=1658652865&sprefix=shark+fish+balloon%2Caps%2C149&sr=8-10)

- Take out the balloon envelope and inflate it with Helium gas. Use this [link](https://www.partycity.com/balloon-time-large-helium-tank-14.9cu-ft-12in-633298.html?extcmp=pla%7CLia%7CGoogle&gclid=Cj0KCQjw2_OWBhDqARIsAAUNTTFcuLXSmsUGsn4tHpC9bbx3VwLVnmTYfgqkL8cs9eoxAmH_OgWX_VsaAl_qEALw_wcB&gclsrc=aw.ds) to buy one if you don't have helium.

- Make sure your blimp is fully inflated and after you inflate your blimp, your blimp should look like this:

  ![]()

- Tie it with string for future use.

## Step 2: Build electronics

To build the whole electronics system:

- Purchase all the electronics: [feather board esp32](https://www.adafruit.com/product/3405), [motor driver board](), [DC motors + propellers]()
- Build your gondola using our [3D printed files]()
- To connect and wire these materials, check [hardware assembly]()
- Put these hardware on the shark fish balloon with [velcro tape](https://www.amazon.com/GOHOOK-Inch-Adhesive-Black-Hook/dp/B08GSHFZYP), you need to follow the instructions in the [hardware assembly](). 

## Step 3: Build software 

### Requirements

To get started, the following requirements should be fulfilled.

- **Arduino IDE** Install Arduino IDE on your laptop and this is for uploading our program to the board


- **Python** Python3.7 or higher version is required for full functions. We recommend you install [Anaconda](https://www.anaconda.com/products/distribution?gclid=Cj0KCQjw2_OWBhDqARIsAAUNTTEpAb0LmpJwzh8JTuAFLq6_szhe4kNi-FylZRn24nbVTP9xn1lFCBMaAgGXEALw_wcB)

### Software setup

There are two things that you need to setup: Arduino IDE and your python environment.

- To set up [featherboard ESP32](https://www.adafruit.com/product/3405), you need to follow the [setup guidance](https://learn.adafruit.com/adafruit-huzzah32-esp32-feather/using-with-arduino-ide). For more details, you can check the full [tutorials](https://learn.adafruit.com/adafruit-huzzah32-esp32-feather). 
- As for python environment, here we will use Anaconda as example. To setup Anaconda on [windows](https://docs.anaconda.com/anaconda/install/windows/) , [Linux](https://docs.anaconda.com/anaconda/install/linux/) and [macOS](https://docs.anaconda.com/anaconda/install/mac-os/).

### Installation

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

Upload program to Featherboard ESP32:



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