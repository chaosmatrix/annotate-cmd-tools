# annotate-cmd-tools
```
All Code Download From Internet,
This Repo Just Do Some Comments For Studying.
If this agains your rights,
Please Contact me to remove it.
```

## numad-0.5+20150602
1. Where To download:
    * https://packages.debian.org/stretch/numad
    * http://deb.debian.org/debian/pool/main/n/numad/numad_0.5+20150602.orig.tar.gz
2. What It Do:
    ```
     Numad is a system daemon that monitors NUMA topology and usage. It will
     attempt to locate processes for optimum NUMA locality and affinity,
     dynamically adjusting to changing system conditions. Numad also provides
     guidance to assist management applications with initial manual binding of
     CPU and memory resources for their processes.
     Via https://packages.debian.org/stretch/numad
    ```
3. What To Do:
    * sysctl -n vm.zone_reclaim_mode = 0
        * turn zone reclaim mode off
    * numactl --interleave=all COMMAND
        * enable NUMA interleaving
    * echo never > /sys/kernel/mm/transparent_hugepage/enabled
        * disable Transparent HugePages, it didn't play nice with NUMA systems
