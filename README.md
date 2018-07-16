# Singularity config for simg-dexpr container

A [Singularity Hub](https://www.singularity-hub.org/) definition for dexpr workflow.

If [Singularity](http://singularity.lbl.gov) is installed locally, the container can be build (needs root access) locally like this:

```bash
sudo singularity build simg-dexpr.simg Singularity
```

The container can alos be downloaded from [Singularity Hub](https://www.singularity-hub.org/) without root access to the local machine like this:

```bash
singularity pull --name "simg-dexpr.simg" sschmeier/simg-dexpr:latest 
```

Then, it can be used, e.g.:

```bash
singularity exec simg-dexpr.simg Rscript test.R > session.txt

# to bind directory not in $HOME
singularity exec --bind /mnt/disk1/seb simg-dexpr.simg Rscript test.R > session.txt

```
