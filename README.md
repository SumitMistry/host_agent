## Introduction
What does this project do? e.g. Cluster Monitor Agent is an internal tool that monitors the cluster resources...it helps the infrastructure team to...

## Design and Architecture

1) Design and Implementation
![caption](https://github.com/sumitJRVS/linux-usage-agent/blob/master/Diagram.jpg)



2,3) Tables and scripts; `host_info` is collecting the hardware information of Linux system /server 1 time and `host_usage` is collecting the server usage and perfmoance abiity over the period of time. `host_info.sh` script executes and insert the information into the table name `host_info`. `host_usage.sh` script executes and insert the CPU activity usage into table name `host_usage`. The last `init.sql` creates the file databse and creates the tables. It also create and strcture the DDL schema into the table

1) Draw a cluster diagram with three Linux host, a DB, and agents
2) Describe tables (no SQL code, just explain their usage)
3) Describe scripts (no code, just explain thier usage)

## Usage
1) How to init database and tables
2) `host_info.sh` usage
3) `host_usage.sh` usage
4) Scheduler setup using command crontab

## Improvements
Things has been improved so far in this projects:
1) Handle hardware updates
2) Instruction to change/customize the scheduler job
3) ...WIP...

`End of README.MD`


