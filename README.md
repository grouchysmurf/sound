# Sound

## Process soundmeter data

### Description

This is a python script to process the sound level data obtained using a Convergence Instruments NSRT_mk2 sound level meter ( <https://convergenceinstruments.com/product/sound-level-meter-data-logger-type-1-microphone-nsrt_mk2/> )

### Intended use

The intended use of this program is to obtain monthly L10, L50 and L90 values from the sound level meter measures. This data is be printed as monthly values during execution and graphs are produced showing:

- The frequency of levels above L10 as a function of time of day every month
- The daily L10, L50 and L90 levels for all provided data
- The daily L10, L50 and L90 levels split by month
- The distribution of L10, L50 and L90 levels split by month
- Comparison graphs (as provided in the repo, comparison is for a single day versus all other days, this should be adjusted as needed)

## Files

### process.py

Process the data. Requires exported XLS files in HH:MM:SS.ms format from the instrument manager software ( <https://convergenceinstruments.com/instrument-manager/> ) Data must be placed in ./data folder . Takes only L50 values from each second; adjust usecols argument on line 13 to modify this setting.

## Prerequisites

Developed using Python 3.7

Requires:

- Numpy
- Pandas (version 0.24.1, there are issues with quantiles on later versions that prevent correct code execution)
- Matplotlib
- Seaborn

## Contributors

Maxime Thibault.

## License

GNU GPL v3

Copyright (C) 2019 Maxime Thibault

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.