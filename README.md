# Hydra Distributed HTTP Benchmark Tool
## Using this container
### Single node mode
Simply run:
```
docker run lucazz/hydra hydra [options] url
```
### Distributed node mode
On the slave nodes, run:
```bash
docker run -d  lucazz/hydra hydra --slave --inet 172.17.0.10
```
And on the master node, run:
``` bash
docker run -it lucazz/hydra hydra --nodes 172.17.0.10 url
```
