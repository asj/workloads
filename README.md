Run performance workloads for the given kernel and configs and compare their results with the past results. Supports fio, vdbench, sysbench (planned) and fsmark (planned). Also compare the underlying block device queues and parameters while running the performance workloads.

Refer to the individual workloads on how to run.

To view the results.
Example:

    $ cd fio
    $ ./analyzedata ./datalocations 
     READ
     -BW-     -io-
     single_d2
     5815MB/s 5234GB Total devices 2 m:single_d:single data/ca-dev143/single_d2/5.4.17-2102.205.7.3.el8uek.x86_64_2
     5963MB/s 5367GB Total devices 2 m:single_d:single data/ca-dev143/single_d2/5.4.17-2102.205.7.3.el8uek.x86_64_nvmever=5_15_1
     4917MB/s 4425GB Total devices 2 m:single_d:single data/ca-dev143/single_d2/5.15.0-2148.0.5.1.el8uek.x86_64_nvmever=5_4_1
    ::

    $ cd vdbench
    $ ./analyzedata ./datalocation 
     WRITE
     IOps   response  mb/sec
     2680.8 26.291    335.1	Total devices 4 RAID1	data/pqe013/5.15.0-0.30.3.el8uek.x86_64/1
     2811.1 26.044    351.3	Total devices 4 RAID1	data/pqe013/5.18.0-rc2+/1
     4215.3 15.648    526.9	Total devices 4 RAID1	data/pqe013/5.4.17-2136.302.6.el8uek.x86_64/1
     5436.4 11.873    679.5	Total devices 4 RAID1	data/pqe013/5.4.0-rc8+/e1f60a6580c0
     2589.6 29.923    323.7	Total devices 4 RAID1	data/pqe013/5.4.0-rc8+/dbb70becde5b
     99525   0.621    12440	Total devices 4 RAID1	data/ca-dev143/5.4.17-2102.205.7.3.el8uek.x86_64

