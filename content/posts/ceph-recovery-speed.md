+++
categories = ["tech"]
date = 2022-09-29T04:48:36Z
title = "What to do when Ceph is taking its bloody time recovering."
tags = [
    "Ceph",
]
+++

## What do do when Ceph is taking its bloody time recovering.

I am rebuilding my main hyperconverged cluster.  Part of that is evacuating all the data from the old nodes.  I took the OSD out of the cluster with `ceph out osd.XX` and the cluster started rebalancing.  Unfortunately it taking forever, luckily I know how to fix it. 

If we looks at the recovery settings, we will notice the max backfills and the max active are low.  The cluster is currently recovering at about 130MB/s

```
root@home-node-3:~# ceph-conf --show-config | egrep "osd_recovery_max_active|osd_recovery_op_priority|osd_max_backfills"
osd_max_backfills = 1
osd_recovery_max_active = 0
osd_recovery_max_active_hdd = 3
osd_recovery_max_active_ssd = 10
osd_recovery_op_priority = 3
```

If we up the number of backfills and max_active it will use more resources but it will recover more quickly.  In fact, setting the `max_backfills` to 4 and `max_active` to 12 we increased the recovery speed to 430MB/s

`ceph tell 'osd.*' injectargs --osd-max-backfills=4 --osd-recovery-max-active=12`

Also see: https://docs.ceph.com/docs/master/dev/osd_internals/backfill_reservation/


