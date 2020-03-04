
```
singularity build --fakeroot debian_8-openmpi_3.sif debian_8-openmpi_3.def
```

```
singularity exec --bind /etc/slurm,/var/run/munge debian_8-openmpi_3.sif /view/openmpi3.1.0_gcc8.1.0/bin/mpirun --version
```

