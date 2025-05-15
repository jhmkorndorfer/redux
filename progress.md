# Daily Progress Log

## Date: 15/05/2025

### Accomplishments
- [] Task 1: Install redux on UBELIX


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