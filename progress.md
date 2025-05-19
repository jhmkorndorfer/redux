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
- [x] Install redux on UBELIX
    - Steps to achieve that again:
        - Before compiling redux on UBELIX we need to install **OpenCV**:
            ``` 
            wget https://github.com/opencv/opencv/archive/4.5.5.tar.gz
            tar -xzf 4.5.5.tar.gz
            cd opencv-4.5.5

            mkdir build && cd build


            cmake .. \
                -DCMAKE_BUILD_TYPE=Release \
                -DCMAKE_INSTALL_PREFIX=$HOME/opt/opencv-install \
                -DBUILD_LIST=core,imgcodecs,imgproc,highgui \
                -DBUILD_EXAMPLES=OFF \
                -DBUILD_TESTS=OFF \
                -DBUILD_PERF_TESTS=OFF \
                -DBUILD_opencv_python=OFF

            make -j 8
            make install
            ```
        - Now for **redux** we need to load all modules and indicate to CMAKE where is OpenCV installed locally.
            ```
            #Inside redux folder create a build directory:
            mkdir build && cd build

            #cmake and indicate the location of OpenCV locally. The following should work everywhere...
            #Lets inform our system of another location for shared libraries
            export LD_LIBRARY_PATH=$HOME/opt/opencv-install/lib:$LD_LIBRARY_PATH
            #Lets inform CMake where to find OpenCV’s config file
            cmake .. \
                -DOpenCV_DIR=$HOME/opt/opencv-install/lib/cmake/opencv4 \
                -DCMAKE_PREFIX_PATH=$HOME/opt/opencv-install
            ```

            make -j 8

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
                - Make it easy for copy pasta:
                    - ml Boost.MPI/1.76.0-gompi-2021a GSL/2.8-GCC-13.3.0 CFITSIO/4.4.1-GCCcore-13.3.0 FFTW.MPI/3.3.10-gompi-2023a zlib/1.2.11-GCCcore-10.3.0 CMake/3.29.3-GCCcore-13.3.0
- Installing opencv using the easybuild 'local' module is only crashing with different versions etc. I think I will end up having to install it locally.

### Learnings
- 


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
- 

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