# TCDiff
This is the code of TCDiff, a Generative AI with Physics-Driven Meteorological Factor Constraint for improving Tropical Cyclone Forecasting.

## Requirements 
* python 3.8.8
* Pytorch 1.11.0 (GPU)

## Data Preparation
First, we need to download all the data we used in TCDiff.
* TCDiff's processed datasets [part1](https://drive.google.com/file/d/1XpfByEZkZHAybXgB5p2YsR5KZhHrtVei/view?usp=drive_link) and [part2](https://drive.google.com/file/d/1aiJaUH035YOIbsS9Q1Y9GGmyKW1HiJU1/view?usp=drive_link)
* TCDiff's [checkpoint](https://drive.google.com/file/d/1H8RKJU_p1vFmIcP5gghg1BMB7oBJ8_zI/view?usp=drive_link)

After completing the downloading, move these file to correct file path.
* Move TCDiff's processed datasets to **/TCDiff**, change the **data_dir** in **TCDiff/configs/baseline.yaml** to **TCDiff/process_data_1D-ENV-ERA5-ALL-WE-NEED-vocen-vodis**
* Move TCDiff's checkpoint to **/TCDiff/experiment/TCDiff_ori**

If you want to process the data yourself, the processing code of TC tilt metrics can be found in **TCDiff/process_data_1D-ENV-ERA5-ALL-WE-NEED-vocen-vodis.py**.

## Train
```python
## change the eval_mode in TCDiff/configs/baseline.yaml to False ##
cd TCDiff
python main.py
```

## Test
```python
## change the eval_mode in TCDiff/configs/baseline.yaml to True ##
cd TCDiff
python main.py
```
## Acknowledgement
Part of our code is borrowed from [MID](https://github.com/Gutianpei/MID). We thank the authors for releasing their code and models.
