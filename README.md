# Lab 05: Realtime
![example workflow](https://github.com/uofu-emb/2024-lab5-jonathan-elmir/actions/workflows/main.yml/badge.svg)

## By: Elmir and Jonathan

In this lab, we measured and gathered data using the oscilliscope. We used the stats function to transfer all the stats to a usb as a png.  Then, we created csv files to create tables for the data measured as depicted in the png and placed them in the DATA directory. From these csv files, we analyzed and calculated jitter and drift, which will be shown in the table below.

We get the drift by doing the following:

drift = (Avg T / Expected T)*3600
expected_drift = abs|drift-expected_drift|

# Activity 1: Table showing data from png + calculations

|   Delay Type   | Period   |   Desired Frequency   |   Actual Frequency  |   Duty Cycle  |     Drift (1hr) |   
|-------|-------|-------|-------|-------|-------|
| sleep       |  199.9988 ms | 5 Hz  | 5.00002 Hz | 50.00 %| 0.02s | 
| sleep_delay |  231.9964 ms | 5 Hz  | 	4.31035 Hz| 50.00 % | ~576s |
| task        |  199.9988 ms | 5 Hz  | 4.99997 Hz | 50.00 % | 0.02s| 
| task_delay  |  232.0056 ms | 5 Hz  | 4.31032 Hz | 50.00 % | ~576s | 
| timer       | 	200.008 ms | 5 Hz  | 4.99997 Hz | 50.00 % | 0.02s | 
| timer_delay | 200.008 ms   | 5 Hz  | 4.99997 Hz | 50.00 %| 0.02s | 


We see that the timer is not affected by the additional work on the thread.

# Activity 2: GPIO Interrupt
When updating the same "busy" task for the GPIO_interrupt, we get that the measured delay between the sync signal and the outpt of the board are: 1.11 microseconds

with the busy work: 10.0084 milliseconds
