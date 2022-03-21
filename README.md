## Synopsis

This project implements 8 clear sky models in a common framework to compare
them with each other and with a reference model and reference measurements.

## License

This project is released under the BSD license.

## Linux Install Instructions
### 1. Clone the repo **with recurvise flag** for git submodules
```bash 
git clone --recursive <git_remote_URL>
```

### 2. Install dependencies (if you don't already have them
```bash
sudo apt-get install p7zip
```

#### 2.1 Install Other depdencies manually:
Make sure you have python2 installed.
```
# Fortran 
sudo apt-get install gfortran

# The NetCDF library is ubiquitously used in Earth science models.
sudo apt-get install libnetcdf-dev libnetcdff-dev

# The GNU Scientific Library (GSL)
sudo apt-get install libgsl-dev 
```

libradtran Library (follow the instructions on the download page):
http://www.libradtran.org/doku.php?id=download
(Note, use `make -j8` to speed things up. Use 8 or whatever number of processes you want.)

Finalize the install by making the library global:
```
sudo make install -j8
```

### 3. Build the project
```bash
make all
```
