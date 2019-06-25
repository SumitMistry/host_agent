## Introduction
Q)What does this project do?
A) Cluster Monitor Agent is an internal tool that monitors the cluster/server/node resources availability   and its usage, its also useful to track and save data into database into a server...it helps the infrastructure team to identify the potential risk to server if it will run out of the disk /pc or RAM storage etc.

## Design and Architecture

1) Design and Implementation
![caption](https://github.com/sumitJRVS/linux-usage-agent/blob/master/Diagram.jpg)

2,3) Tables and scripts; `host_info` is collecting the hardware information of Linux system /server 1 time and `host_usage` is collecting the server usage and perfmoance abiity over the period of time. `host_info.sh` script executes and insert the information into the table name `host_info`. `host_usage.sh` script executes and insert the CPU activity usage into table name `host_usage`. The last `init.sql` creates the file databse and creates the tables. It also create and strcture the DDL schema into the table



## Usage
1) How to init database and tables
        file `init.sql` contains script for table initialization, but for the db init need to create posrtgresql db and run via docker.
2) `host_info.sh` usage
        `host_info.sh` is used to collection CPU parameters and parsing it to th
e insert table query to make db. It makes table name `host_info`
3) `host_usage.sh` usage
        `host_usage.sh` is used to collect CPU/RAM/Storage etc HW resources from
 server and insert to the table `host_usage`
4) Scheduler setup using command crontab
        crontab is used too setup scheduled event command script for us automatically defined on period range from seconds, day, months etc.


## Improvements
Things has been improved so far in this projects:
1) Handle hardware updates
2) Instruction to change/customize the scheduler job
3) ...WIP...

`End of README.MD`


