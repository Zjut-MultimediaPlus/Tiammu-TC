# Tianmu-TC
This is the code of Tianmu-TC, a Generative AI with Physics-Driven Meteorological Factor Constraint for improving Tropical Cyclone Forecasting.

## Requirements 
* python 3.8.8
* Pytorch 1.11.0 (GPU)

## Data Preparation
First, we need to download all the data we used in Tianmu-TC.
* Tianmu-TC's processed datasets [part1](https://drive.google.com/file/d/1XpfByEZkZHAybXgB5p2YsR5KZhHrtVei/view?usp=drive_link) and [part2](https://drive.google.com/file/d/1aiJaUH035YOIbsS9Q1Y9GGmyKW1HiJU1/view?usp=drive_link)
* Tianmu-TC's [checkpoint](https://drive.google.com/file/d/1H8RKJU_p1vFmIcP5gghg1BMB7oBJ8_zI/view?usp=drive_link)

After completing the downloading, move these file to correct file path.
* Move Tianmu-TC's processed datasets to **/Tianmu-TC**, change the **data_dir** in **Tianmu-TC/configs/baseline.yaml** to **Tianmu-TC/process_data_1D-ENV-ERA5-ALL-WE-NEED-vocen-vodis**
* Move Tianmu-TC's checkpoint to **/Tianmu-TC/experiment/Tianmu-TC_ori**

If you want to process the data yourself, the processing code of TC tilt metrics can be found in **Tianmu-TC/process_data_1D-ENV-ERA5-ALL-WE-NEED-vocen-vodis.py**.

## Train
```python
## change the eval_mode in Tianmu-TC/configs/baseline.yaml to False ##
cd Tianmu-TC
python main.py
```

## Test
```python
## change the eval_mode in Tianmu-TC/configs/baseline.yaml to True ##
cd Tianmu-TC
python main.py
```
## Acknowledgement
Part of our code is borrowed from [MID](https://github.com/Gutianpei/MID). We thank the authors for releasing their code and models.
