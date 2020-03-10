## Step 1: Build base container
```
singularity build --fakeroot debian_8-base.sif debian_8-base.def
```

## Step 2 a: Build container with OpenMPI
```
singularity build --fakeroot debian_8-openmpi_3.sif debian_8-openmpi_3.def
```

### Execute mpirun
```
singularity exec --bind /etc/slurm,/var/run/munge debian_8-openmpi_3.sif mpirun --version
```

## Step 2 b: Build container, which uses R3BRoot
```
singularity build --fakeroot debian_8-r3broot.sif debian_8-r3broot.def
```

### Run simulation
```
singularity run --bind /cvmfs/fairroot.gsi.de,/lustre/rz/kresan debian_8-r3broot.sif
```

### Path to image files

 - /lustre/rz/kresan/debian_8-base.sif
 - /lustre/rz/kresan/debian_8-openmpi_3.sif
 - /lustre/rz/kresan/debian_8-r3broot.sif

