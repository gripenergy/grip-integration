This repository holds the files needed to set up a docker container for the grip-absorption/gridlab-d simulation.

### To build the container do the following
```
$ docker build -t gridlabd-slacgrip .
```
or just `build.sh`

### To launch the container starting at the test directory
```
$ docker run -it --rm -v $(pwd):/opt/tests --workdir /opt/tests gridlabd-slacgrip
```
or just `launch.sh`

### To run the julia server tests

```
$ docker run -it --rm -v $(pwd):/opt/build --workdir /opt/build/python gridlabd-slacgrip

[root@<docker-id> python]# python julia_server.test.py
```

### To run the example Gridlab-D start script and on_commit hooks

```
$ docker run -it --rm -v $(pwd):/opt/build --workdir /opt/build/python gridlabd-slacgrip

[root@<docker-id> python]# python run_gridlabd_main.py
```
### To run a test of optimization in julia
```
$ docker run -it --rm -v $(pwd):/opt/build --workdir /opt/build/julia gridlabd-slacgrip

[root@<docker-id> python]# julia test_jump.jl
```
