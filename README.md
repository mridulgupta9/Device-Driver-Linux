# Device-Driver-Linux
## Objective
Design of unavailable design drivers for using controller as mouse. This is our work towards completition of CSN232 (Operating System).

## Project Detail
This project has basically two parts.
1. To read inputs from controller and give output to the kernel so that we can read it further.
2. Read the inputs from the kernel space and create different functions to use the written data.

## How to use?
Go the directory of project --> Open Terminal
```
usr@username:/user/project_dir$make
```
So, this will make filename.ko (in our case joy2mouse.ko)
now run this command
```
usr@username:/user/project_dir$sudo insmode joy2mouse.ko
```
Now this will load the module.
Now to activate the driver
```
usr@username:/user/project_dir$ls -l /dev/input | grep js2ms   #take the maximum number from here
usr@username:/user/project_dir$cat /dev/input/js2ms#/           #for ex. js2ms0 js2ms1 then replace # with 1.
```
Now you are good and enjoy!
