
Change docker daemon startup setting as following

/usr/bin/docker.io -d -H tcp://0.0.0.0:2375 --label computing_unit=opencl-2_0


(A) Create swarm and cluster
-----------
docker -H tcp://0.0.0.0:2375 run --rm swarm create
(this id will be used by token as cluster ID)

docker -H tcp://0.0.0.0:2375 run -d swarm join --addr=220.135.180.119:2375 token://c019340ab221db663eb344f2a844bc89

swarm manage -H tcp://220.135.180.119:4444 token://c019340ab221db663eb344f2a844bc89



(B)Test it through manage ip:port
------------
docker -H tcp://220.135.180.119:4444 info

docker -H tcp://220.135.180.119:4444 ps


(C) Then launch a container
-------------

docker -H tcp://220.135.180.119:4444 run -e constraint:computing_unit==opencl-2_0 -it ubuntu/amd_opencl_2_0:v01 /bin/bash



reference: 
----------------
https://github.com/docker/swarm/tree/master/scheduler/filter

https://github.com/docker/swarm

