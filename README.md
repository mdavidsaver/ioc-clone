ioc-clone
=========

Assist in off-line creation of EPICS OPI (OPerator Interface) screens.
Creates a `.db` file which can be used with `softIoc` to provide serve
up a snapshot of PV values when the script was run.

Has some knowledge about EPICS Base record types to facilitate
simulation of active alarm conditions.

```sh
$ cat pvlist.txt
pv:name
another:name
$ ioc-clone pvlist.txt sim.db
```

Copy `sim.db` to a different network!

```sh
$ softIoc -d sim.db
```
