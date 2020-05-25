# Pretrained models

The pretrained [4stems model](https://github.com/deezer/spleeter/blob/master/spleeter/resources/4stems.json) has the following performances when tested on the [musDB](https://sigsep.github.io/datasets/musdb.html) test set:

|           |Spleeter Mask  |Spleeter MWF   |
|-----------|---------------|---------------|
| Vocals SDR|6.55           |6.86           |
| Vocals SIR|15.19          |15.86          |
| Vocals SAR|6.44           |6.99           |
| Vocals ISR|12.01          |11.95          |
| Bass SDR  |5.10           |5.51           |
| Bass SIR  |10.01          |10.30          |
| Bass SAR  |5.15           |5.96           |
| Bass ISR  |9.18           |9.61           |
| Drums SDR |5.93           |6.71           |
| Drums SIR |12.24          |13.67          |
| Drums SAR |5.78           |6.54           |
| Drums ISR |10.50          |10.69          |
| Other SDR |4.24           |4.55           |
| Other SIR |7.86           |8.16           |
| Other SAR |4.63           |4.88           |
| Other ISR |9.83           |9.87           |

The first column of this table can be reproduced using the following command (you need to download musdb first and to put it into the <musdb path> folder):
```bash
spleeter evaluate -p spleeter:4stems -o spleeter_mask_results --mus_dir <musdb path>
```
The second column can be reproduced using the following command:
```bash
spleeter evaluate -p spleeter:4stems -o spleeter_mwf_results --mus_dir <musdb path> -m
```

# Training on musdb

It is possible to train a model with the [musDB](https://sigsep.github.io/datasets/musdb.html) train dataset.
To do so use the [configs/musdb_config.json](https://github.com/deezer/spleeter/blob/master/configs/musdb_config.json):
```bash
spleeter train --verbose -p configs/musdb_config.json -d <musdb path>
```
This should provide the following results on the dataset:

|           |SDR     |SAR     |SIR      |ISR     |
|-----------|--------|--------|---------|--------|
| Vocals    |5.10    |5.44    |12.45    |9.58    |
| Drums     |5.15    |5.25    |10.68    |8.89    |
| Bass      |4.27    |5.42    |7.23     |9.38    |
| Other     |3.21    |3.89    |5.37     |7.80    |

Once the model trained, the results of this table can be generated with:
```bash
spleeter evaluate -p configs/musdb_config.json -o musdb_trained_spleeter_results --mus_dir <musdb path> -m
```
