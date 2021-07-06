This is an implementation of [Discrete Graph Structure Learning for Forecasting Multiple Time Series](https://github.com/chaoshangcs/GTS) for battery parameter data.

Variables considered- Voltage (V), Charge Capacity (Ah), Battery Level 

Paper: "[Discrete Graph Structure Learning for Forecasting Multiple Time Series](https://openreview.net/pdf?id=WEHSlH5mOk)", ICLR 2021.

## Installation

Install the dependency using the following command:

```bash
pip install -r requirements.txt
```

## Data Preparation

Data files can be found in the 'Datasets used' folder.

Run the following commands to generate train/test/val dataset at  `data/{CHARGE}/{train,val,test}.npz`.
```bash
# Create data directories
mkdir -p data/CHARGE

# Generate training data
python -m scripts.generate_training_data --output_dir=data/CHARGE --traffic_df_filename=data/charge.h5
```
## Train Model

When you train the model, you can run:

```bash
# Use METR-LA dataset
python train.py --config_filename=data/model/para_charge.yaml
```
