Run with vexcl/sort application between docker container and native env.

[ Native env]

chester@cheser-System-Product-Name:/tmp/opencl$ time ./sort

seed: 1425380037
1. AMD A10-7850K Radeon R7, 12 Compute Cores 4C+8G (AMD Accelerated Parallel Processing)

2. AMD A10-7850K Radeon R7, 12 Compute Cores 4C+8G (AMD Accelerated Parallel Processing)


Running 6 test cases...

*** No errors detected

real    0m16.068s

user    0m17.402s

sys     0m8.621s


chester@cheser-System-Product-Name:/tmp/opencl$ time ./sort

seed: 1425380056
1. AMD A10-7850K Radeon R7, 12 Compute Cores 4C+8G (AMD Accelerated Parallel Processing)

2. AMD A10-7850K Radeon R7, 12 Compute Cores 4C+8G (AMD Accelerated Parallel Processing)


Running 6 test cases...

*** No errors detected

real    0m16.213s

user    0m17.794s

sys     0m9.125s


-----------------------------------

[ Docker container ]

root@0dce4907ee97:/tmp/opencl# time ./sort
seed: 1425380076
1. AMD A10-7850K Radeon R7, 12 Compute Cores 4C+8G (AMD Accelerated Parallel Processing)

2. AMD A10-7850K Radeon R7, 12 Compute Cores 4C+8G (AMD Accelerated Parallel Processing)

Running 6 test cases...

*** No errors detected

real    0m15.873s

user    0m17.185s

sys     0m7.688s

root@0dce4907ee97:/tmp/opencl# time ./sort
seed: 1425380109
1. AMD A10-7850K Radeon R7, 12 Compute Cores 4C+8G (AMD Accelerated Parallel Processing)

2. AMD A10-7850K Radeon R7, 12 Compute Cores 4C+8G (AMD Accelerated Parallel Processing)


Running 6 test cases...

*** No errors detected

real    0m15.878s

user    0m17.184s

sys     0m8.103s


