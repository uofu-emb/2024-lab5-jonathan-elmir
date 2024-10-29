# Lab 05: Realtime
![example workflow](https://github.com/uofu-emb/2024-lab5-jonathan-elmir/actions/workflows/main.yml/badge.svg)

## By: Elmir and Jonathan

In this lab, we measured and gathered data using the oscilliscope. We used the stats function to transfer all the stats to a usb as a png.  Then, we created csv files to create tables for the data measured as depicted in the png and placed hthem in the DATA directory. From these csv files, we analyzed and calculated jitter and drift, which will be shown in the table below.

# Table showing data from png + calculations

|   Delay Type   |   Desired Frequency   |   Actual Frequency  |   Duty Cycle  |   Period   |   Jitter   |   Drift   |
|-------|-------|-------|-------|-------|-------|-------|
| sleep | 1 Hz |  1 Hz | Row 1 | Row 1 | Row 1 | Row 1 |
| sleep_delay |  1 Hz | Row 2 | Row 2 | Row 2 | Row 2 | Row 2 |
| task |  1 Hz | Row 3 | Row 3 | Row 3 | Row 3 | Row 3 |
| task_delay |  1 Hz | Row 4 | Row 4 | Row 4 | Row 4 | Row 4 |
| timer | 1 Hz | Row 5 | Row 5 | Row 5 | Row 5 | Row 5 |
| timer_delay | 1 Hz | Row 6 | Row 6 | Row 6 | Row 6 | Row 6 |

