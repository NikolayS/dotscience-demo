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
