# Report of Monaco 2018 Racing

## Overview

This is a command line application that generates a report for the racers of a racing cup. It creates a list 
of the best racers who will go to the second round and continue their competition. It evaluates the provided data and 
returns the result.


## Modules that are used
- [argparse](https://docs.python.org/3/library/argparse.html)
- [colorama](https://pypi.org/project/colorama/)

## How to install

> pip install -i https://test.pypi.org/simple/ racers-report==1.0.2

## How to fill key files
You need to provide a path to directory where your 'start.log', 'end.log' and 'abbreviations.txt' 
files are located.

- 'stand.log' file where start time of the lap for each racer is located
- 'end.log' file where end time of the lap for each racer is located
- 'abbreviations.txt' file with abbreviations explanations are located

### Examples of records for each file are presented below

#### start.log file
- KRF2018-05-24_12:03:01.250
- SVM2018-05-24_12:18:37.735

#### end.log file

- MES2018-05-24_12:05:58.778
- RGH2018-05-24_12:06:27.441

#### abbreviations.txt file
- EOF_Esteban Ocon_FORCE INDIA MERCEDES
- FAM_Fernando Alonso_MCLAREN RENAULT

## Usage

If you want to get list of racers who go to the next stage, type the following in the command line:

> py -m racers_report --files "<path_to_the_directory_with_needed_files>"

You can select the order in which racers will appear, with the help either '--asc asc' or '--desc desc':

> py -m racers_report --files "<path_to_the_directory_with_needed_files>" --desc desc

In order to obtain information only for the selected racer, type the following cmd:

> py -m racers_report --files "<path_to_the_directory_with_needed_files>" --driver "<name_of_the_driver>"
