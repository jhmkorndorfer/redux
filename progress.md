# Daily Progress Log

## Date: 16/05/2025

### Accomplishments
- [] Install redux on UBELIX



### Challenges
- Still working on installing OpenCV on UBELIX as a local module. It always crashes somewhere but I cannot get the error... trying different versions of the OpenCV module now.
    - [] Install OpenCV module on UBELIX. That is going to remain here for a while. Could not make this work using these instructions: https://hpc-unibe-ch.github.io/software/installing/easybuild/. 

### Learnings
- Check WiKi shared by Lucia: https://dubshen.astro.su.se/wiki/index.php/Redux

---

## Date: 15/05/2025

### Accomplishments
- [] Install redux on UBELIX


### Challenges
- Figure it out which modules on UBELIX will Fulfill the dependencies of redux.
    - 1st try using module avail to check where I can find the dependencies:
        - module avail boost
        - module avail gsl
        - module avail opencv
        - module avail cfitsio
        - module avail fftw
        - module avail zlib
            - Lets try to following modules:
                - ml Boost.MPI/1.76.0-gompi-2021a
                - ml GSL/2.8-GCC-13.3.0
                - opencv NOT FOUND YET, lets see what happens...
                - ml CFITSIO/4.4.1-GCCcore-13.3.0
                - ml FFTW.MPI/3.3.10-gompi-2023a  (using the same as we used for stic)
                - ml zlib/1.2.11-GCCcore-10.3.0
                - Also need to load CMake. Trying the newest available: ml CMake/3.29.3-GCCcore-13.3.0
- Installing opencv using the easybuild 'local' module is only crashing with different versions etc. I think I will end up having to install it locally.

### Learnings
- Check WiKi shared by Lucia: https://dubshen.astro.su.se/wiki/index.php/Redux


## Date: 16/05/2025

### Accomplishments
- [] Install OpenCV module on UBELIX
- [] Install redux on UBELIX
- [] Trying to install opencv using these instructions: https://hpc-unibe-ch.github.io/software/installing/easybuild/. This will allow us to have it as a 'local' easybuild module. 


### Challenges
- Still working on installing OpenCV on UBELIX as a local module. It always crashes somewhere but I cannot get the error... trying different versions of the OpenCV module now.

### Learnings
- Check WiKi shared by Lucia: https://dubshen.astro.su.se/wiki/index.php/Redux

---

## Date: 15/05/2025

### Accomplishments
- [] Install redux on UBELIX
- [] Trying to install opencv using these instructions: https://hpc-unibe-ch.github.io/software/installing/easybuild/. This will allow us to have it as a 'local' easybuild module. 


### Challenges
- Figure it out which modules on UBELIX will Fulfill the dependencies of redux.
    - 1st try using module avail to check where I can find the dependencies:
        - module avail boost
        - module avail gsl
        - module avail opencv
        - module avail cfitsio
        - module avail fftw
        - module avail zlib
            - Lets try to following modules:
                - ml Boost.MPI/1.76.0-gompi-2021a
                - ml GSL/2.8-GCC-13.3.0
                - opencv NOT FOUND YET, lets see what happens...
                - ml CFITSIO/4.4.1-GCCcore-13.3.0
                - ml FFTW.MPI/3.3.10-gompi-2023a  (using the same as we used for stic)
                - ml zlib/1.2.11-GCCcore-10.3.0
                - Also need to load CMake. Trying the newest available: ml CMake/3.29.3-GCCcore-13.3.0
- Installing opencv using the easybuild 'local' module is only crashing with different versions etc. I think I will end up having to install it locally.

### Learnings
- Check WiKi shared by Lucia: https://dubshen.astro.su.se/wiki/index.php/Redux

---

## Date: 12/05/2025

### Accomplishments
- [x] Task 1: Forking repository.
- [x] Task 2: Copy everything to UBELIX sever.
- [x] Task 3: Copy everything to miniHPC sever.


### Challenges
- NA

### Learnings
- NA

---