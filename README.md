# Solar Panel Detection

## Overview

The Solar Panel Detection project is part of my internship at DLR in Munich. Until now we were using old school CNNs to monitor panels but the goal is to use Foundation Models.
I am fine-tuning Prithvi Foundation Model to be able to detect every roof solar panels in Germany using the DOP20 dataset provided. Here I will publish everything that can be published.
## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Introduction

Solar energy is a renewable energy source that can significantly reduce carbon footprints. Detecting solar panels accurately is essential for assessing solar energy potential and monitoring installations especially in Germany. This project takes part in the EO Solar platform dev, see https://eosolar.dlr.de/

## Dataset: PV4GER
The training data is sourced from the **PV4GER** dataset available on **Zenodo**:
- **Source:** [Zenodo - PV4GER Dataset](https://zenodo.org/record/4507000)
- **Content:** 4,027 HDF5 tiles of satellite imagery (Germany).
- **Processing:** Custom data loader to handle 5D temporal dimensions and 6-band spectral requirements for Prithvi compatibility.
My goal was to get the same mIoU as Prithvi-300 benchmark on solar panel detection 


## Installation
To get started with the Solar Panel Detection project, clone the repository and install the necessary dependencies:

```bash
git clone https://github.com/LouisFOU/Solar-Panel-Detection.git
cd Solar-Panel-Detection
pip install -r requirements.txt
```

## Usage
After installation, you can use the detection module as follows:

```bash
python detect_solar_panels.py --input <image_path>
```

Replace `<image_path>` with the path to the image containing potential solar panels.

## Contributing
Contributions are welcome! Please open an issue or submit a pull request for any enhancements or bug fixes.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
