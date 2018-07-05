# dotscience-demo

Start dotscience with settings:

* Project dot: `dotscience-project`
* Data dots: `agent1, agent2, combined-houses, model`

```
cd /Volumes/dotscience
```
```
git clone https://github.com/dotmesh-io/dotscience-demo
```
```
dotscience-demo/setup.sh
```

This will copy source data into agent1 and agent2, and copy the notebook into your project dot.

Ignore errors like `could not copy extended attributes to X: Operation not permitted`, they are just warnings.

## cleanup

Stop the dotscience app to stop it restarting things.

```
docker rm -f dotscience-app samba dotscience-committer
```
```
for X in $(dm list -H |cut -f 1); do dm dot delete -f $X; done
```
*WARNING* This will delete all your dots, no turning back

If you want to be extra sure it'll work when you spin back up, ensure the result of the following is empty:
```
docker run -it --rm --privileged --pid=host justincormack/nsenter1 /bin/sh -c "ls /var/lib/dotmesh/container_mnt/admin"
```
