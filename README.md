# SLA_Breach_LocalHardDrive_Repo
 
 
# Calculate_SLA_Breach_Time

## Table of Contents
  * [What: Project Overview](#what-project-overview)
  * [Project Problem Statement](#project-problem-statement)
  * [Why: Motivation](#why-motivation)
  * [How: Process Involved](#how-process-involved)
  * [Directory Tree](#directory-tree)
  

## WHAT: Project Overview 
Simple Project: We calculate SLA(Service Level Agreement) breach time for a typical manufacturing unit based on certain business constraints. Input is a data excel file and output is excel file with breach time as a new generated column

### Project Problem Statement
Assessment: 1 – Decoding the SLA breach time

Refer – Decode tab in the input data file

CASE : The team works in 3 shifts  8 am – 5 pm, for the following time zones : Singapore, Dresden (Germany) and USA (EST).
We need to publish the SLA breach time based on request approval time for the team to monitor compliance to the TAT SLA.

Below are the scenarios :

SLA is for working hours only (excluding weekends)
Any request approved after before 8 AM and after 5 PM in the respective time zones, the SLA shall start on next working hour.
Example – if SLA is 4 working hours and if a request is approved at 6:00 PM, then SLA should start in next working day 8 AM for that time zone

Any request approved during the shift hours but the SLA hours goes past 5 PM of that day then balance SLA time to be added to next working day
Example- if SLA is 4 working hours and if a request is approved at 4 PM then program should consider 1 hour of the same day and balance 3 hours to be added to next working day in that time zone

TASK: Given all the above conditions, calculate the SLA breach time, for an SLA of 4 working hours. Populate the SLA breach time on Column D of the file.

## WHY: Motivation
This problem was handed to be over by a friend in manufacturing industry and I thought I will convert it to python project to get the desired output for him.

## HOW: Process Involved
- This section mentions EDA Process, ML algorithms, Libraries used if any etc

I used simple Python programming knowledge with numpy, pandas and lambda function to get the desired output.

<!--## Directory Tree 
```
├── app 
│   ├── __init__.py
│   ├── main.py
│   ├── model
│   ├── static
│   └── templates
├── config
│   ├── __init__.py
├── processing
│   ├── __init__.py
├── requirements.txt
├── runtime.txt
├── LICENSE
├── Procfile
├── README.md
└── wsgi.py
```
-->

## Directory Tree
```
|--   app
|     |-- Readme.md
|     |-- main.py
|     |-- data
|          |-- Input_Data_Files -- sla_breach_time.xlsx
|          |-- Output_Data_Files -- output_data_sla_breach_time.xlsx
```

- Readme.md is the markdown sensitive readme file which you are reading currently
- data folder has sub folders Input_Data_Files and Output_Data_Files. They contain the necessary input and outpur files of interest.
- Have used relative paths while reading and writing files
- File starting with main_ is the main python file you need to execute(in editors like jupyter notebook or google colab)

